## `aerospike:ee-5.6.0.9`

```console
$ docker pull aerospike@sha256:690b667b7974b2257c60417b962f2e04e6ee20adf9cf8830fdc58201be52a025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ee-5.6.0.9` - linux; amd64

```console
$ docker pull aerospike@sha256:327bffeda0018df1bc3f3a779fee1e6ab66aad3ed0797c1bfded4ef2cfbc6b62
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82471737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa99f8a8479fcb2c0a82da40f966e234b486cb13c5dc4a9f5e6f8f87b4f1b4c6`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:43 GMT
ADD file:45f5dfa135c848a348382413cb8b66a3b1dac3276814fbbe4684b39101d1b148 in / 
# Thu, 22 Jul 2021 00:45:44 GMT
CMD ["bash"]
# Thu, 05 Aug 2021 00:19:21 GMT
ENV AEROSPIKE_VERSION=5.6.0.9
# Thu, 05 Aug 2021 00:19:21 GMT
ENV AEROSPIKE_SHA256=c7b16a194bc6a025b7f97f962a4102da255c38bdf99ff59bea15349be3bd02cb
# Thu, 05 Aug 2021 00:19:42 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 python3-distutils lua5.2 gettext-base libldap-dev libcurl4-openssl-dev   && wget "https://www.aerospike.com/enterprise/download/server/${AEROSPIKE_VERSION}/artifact/debian10" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Thu, 05 Aug 2021 00:19:42 GMT
COPY file:7d75174e09b209cf7f56b715636c2b8e08dd083d548e8cdc8517cabd512600b5 in /etc/aerospike/aerospike.template.conf 
# Thu, 05 Aug 2021 00:19:42 GMT
COPY file:31b6a51a1d9d91f22433472f07f6ddfe3cea3bb07f460dd69c4187bc7fd20fdf in /entrypoint.sh 
# Thu, 05 Aug 2021 00:19:43 GMT
EXPOSE 3000 3001 3002
# Thu, 05 Aug 2021 00:19:43 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Thu, 05 Aug 2021 00:19:43 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:33847f680f63fb1b343a9fc782e267b5abdbdb50d65d4b9bd2a136291d67cf75`  
		Last Modified: Thu, 22 Jul 2021 00:50:35 GMT  
		Size: 27.1 MB (27145795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32733a077fa8d1e3572591cf1b2a52049294d896bfbb17d607c15a0228d2249a`  
		Last Modified: Thu, 05 Aug 2021 00:20:28 GMT  
		Size: 55.3 MB (55323862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a547d74f4c7d7a67bc85c0578f1c29ac5b7e92e71505d9b1a36445f7ca59467`  
		Last Modified: Thu, 05 Aug 2021 00:20:17 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8e25daf2401ee48a4570bc03fca12ab366ab502564a431b00bd75d8cf383ad7`  
		Last Modified: Thu, 05 Aug 2021 00:20:17 GMT  
		Size: 908.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
