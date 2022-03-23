## `aerospike:ce-5.7.0.12`

```console
$ docker pull aerospike@sha256:c755d711b3ebe501d441f42b67c589859fd96778a93f67a348be3c704d29ee5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ce-5.7.0.12` - linux; amd64

```console
$ docker pull aerospike@sha256:794df238dfec86f14bd8f8d6fc8a5785541b4eeabce4b1b3b194526a04172361
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.5 MB (81536970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f8b7d6cce3b63c116470438a7698d6fb21d70fecec6b84fb84004a1d170e4f5`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:26 GMT
ADD file:7f5787c324936e09d339f9426eec4a0120431e2a4b6ccb0db28b94d61f074ab2 in / 
# Thu, 17 Mar 2022 04:04:27 GMT
CMD ["bash"]
# Wed, 23 Mar 2022 15:19:19 GMT
ENV AEROSPIKE_VERSION=5.7.0.12
# Wed, 23 Mar 2022 15:19:43 GMT
ENV AEROSPIKE_SHA256=a763ca06c40d74aa7a1417e446aaa8f592e2367f127304495f6c9392e5b07ffd
# Wed, 23 Mar 2022 15:20:01 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 python3-distutils lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian10.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Wed, 23 Mar 2022 15:20:01 GMT
COPY file:1897c4aae07efbc61bf2d8c2c7b0dfb0990174e11cc787eac71d5adf767abaed in /etc/aerospike/aerospike.template.conf 
# Wed, 23 Mar 2022 15:20:01 GMT
COPY file:e1d47057fdb4c34c118f7ba5898161c386b475cba70907a4ae483866cf07335b in /entrypoint.sh 
# Wed, 23 Mar 2022 15:20:01 GMT
EXPOSE 3000 3001 3002
# Wed, 23 Mar 2022 15:20:01 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Wed, 23 Mar 2022 15:20:01 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:a4b007099961706d45bdb3eb0a3aab719916c3e36d6da7577b0c9060260e65f8`  
		Last Modified: Thu, 17 Mar 2022 04:10:54 GMT  
		Size: 27.2 MB (27153828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec95fc95c1a0031366e9b5b185a4fee32a138ae0bebb387d336924b29ef1c40`  
		Last Modified: Wed, 23 Mar 2022 15:20:38 GMT  
		Size: 54.4 MB (54381119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65f5db72241d4b744ba2ca6cabb5740fb27dbf7095ef350cb5832cfa59ff8b6`  
		Last Modified: Wed, 23 Mar 2022 15:20:30 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eaf3e068a1f1e4e7516a7987e1cedd31a690a47de1d7dd59cb4d54c18aab3d8`  
		Last Modified: Wed, 23 Mar 2022 15:20:30 GMT  
		Size: 883.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
