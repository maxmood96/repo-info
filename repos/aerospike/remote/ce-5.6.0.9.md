## `aerospike:ce-5.6.0.9`

```console
$ docker pull aerospike@sha256:10d073c67e6faa94dc88af990c2a28c25b0308676661e63baa1a8a51472f2353
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ce-5.6.0.9` - linux; amd64

```console
$ docker pull aerospike@sha256:0d1f0812f70ae5f6acf8c884c70e2bc185d2ee2be6b85d1641cf90c33d7d9af9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.6 MB (80606060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eacf0dfe5e3491b0713688591b3830da7782e0ad678447352c44f131b06245d`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:43 GMT
ADD file:45f5dfa135c848a348382413cb8b66a3b1dac3276814fbbe4684b39101d1b148 in / 
# Thu, 22 Jul 2021 00:45:44 GMT
CMD ["bash"]
# Thu, 05 Aug 2021 00:19:21 GMT
ENV AEROSPIKE_VERSION=5.6.0.9
# Thu, 05 Aug 2021 00:19:47 GMT
ENV AEROSPIKE_SHA256=82b15902420752273e22405d929e43a7062e9c84b604e2c1e9f27d26c8ae0aad
# Thu, 05 Aug 2021 00:20:05 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 python3-distutils lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian10.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Thu, 05 Aug 2021 00:20:05 GMT
COPY file:1897c4aae07efbc61bf2d8c2c7b0dfb0990174e11cc787eac71d5adf767abaed in /etc/aerospike/aerospike.template.conf 
# Thu, 05 Aug 2021 00:20:06 GMT
COPY file:e1d47057fdb4c34c118f7ba5898161c386b475cba70907a4ae483866cf07335b in /entrypoint.sh 
# Thu, 05 Aug 2021 00:20:06 GMT
EXPOSE 3000 3001 3002
# Thu, 05 Aug 2021 00:20:06 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Thu, 05 Aug 2021 00:20:06 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:33847f680f63fb1b343a9fc782e267b5abdbdb50d65d4b9bd2a136291d67cf75`  
		Last Modified: Thu, 22 Jul 2021 00:50:35 GMT  
		Size: 27.1 MB (27145795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b977877b0628383e8aeafa07e01fc1b38c4450572d11f45ea69342f81cf47e4b`  
		Last Modified: Thu, 05 Aug 2021 00:20:44 GMT  
		Size: 53.5 MB (53458245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab83624acdd1a32f2b912b758473e17855840c8343f4ad5a598b1c6d5f2cab5c`  
		Last Modified: Thu, 05 Aug 2021 00:20:36 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80647a715fe929ca4f3a70f947c18ab57e03d1baab139b23f1774b4508ef3904`  
		Last Modified: Thu, 05 Aug 2021 00:20:36 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
