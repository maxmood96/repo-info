<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `aerospike`

-	[`aerospike:ce-5.6.0.8`](#aerospikece-5608)
-	[`aerospike:ee-5.6.0.8`](#aerospikeee-5608)

## `aerospike:ce-5.6.0.8`

```console
$ docker pull aerospike@sha256:febd266ae249a20660a2e6cfd10720b0a541c905c891141d0fb17ea3778df0e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ce-5.6.0.8` - linux; amd64

```console
$ docker pull aerospike@sha256:e1d329bcfde306b74bee4700aca30854b8b70b10039bc78c74fbb6d2b9d68107
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.6 MB (80605689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb1afec3f591c811eee83f2e72d0f3c54b402dd7d5be168823baddfc07d3627`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:43 GMT
ADD file:45f5dfa135c848a348382413cb8b66a3b1dac3276814fbbe4684b39101d1b148 in / 
# Thu, 22 Jul 2021 00:45:44 GMT
CMD ["bash"]
# Fri, 23 Jul 2021 12:30:11 GMT
ENV AEROSPIKE_VERSION=5.6.0.8
# Fri, 23 Jul 2021 12:30:37 GMT
ENV AEROSPIKE_SHA256=cf03a8af51be333caea4dd98ae02b0d4bd22b570732a7b8eb59380015f646cdd
# Fri, 23 Jul 2021 12:30:55 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 python3-distutils lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian10.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Fri, 23 Jul 2021 12:30:56 GMT
COPY file:1897c4aae07efbc61bf2d8c2c7b0dfb0990174e11cc787eac71d5adf767abaed in /etc/aerospike/aerospike.template.conf 
# Fri, 23 Jul 2021 12:30:56 GMT
COPY file:e1d47057fdb4c34c118f7ba5898161c386b475cba70907a4ae483866cf07335b in /entrypoint.sh 
# Fri, 23 Jul 2021 12:30:56 GMT
EXPOSE 3000 3001 3002
# Fri, 23 Jul 2021 12:30:56 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Fri, 23 Jul 2021 12:30:56 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:33847f680f63fb1b343a9fc782e267b5abdbdb50d65d4b9bd2a136291d67cf75`  
		Last Modified: Thu, 22 Jul 2021 00:50:35 GMT  
		Size: 27.1 MB (27145795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb6ec6b43599540084c6e73af90c8c75e2b186e4adb475eda0c39ca9fc09732`  
		Last Modified: Fri, 23 Jul 2021 12:31:32 GMT  
		Size: 53.5 MB (53457873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7af9a32551bc6a6c1bca78b9a4a8c9c6ca9f88ffe49dc8a745bde3c1a2d347a`  
		Last Modified: Fri, 23 Jul 2021 12:31:24 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f42d12154c412e50d861d22cf360c1ee5b834c1d178caa558e9d20eeb8ce6a6c`  
		Last Modified: Fri, 23 Jul 2021 12:31:24 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:ee-5.6.0.8`

```console
$ docker pull aerospike@sha256:7a1ec51a1abd7ac53ce6c6305602db0c852241456197762afafae14797f076d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ee-5.6.0.8` - linux; amd64

```console
$ docker pull aerospike@sha256:2c204434dd4ff4c0cc27830f4ca421027a2a528438f1a712801df6d1a8728304
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82472137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8725aac0543db20be50492f38422b34711f71aea4d7e3c3e6f3add8a544b95cf`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:43 GMT
ADD file:45f5dfa135c848a348382413cb8b66a3b1dac3276814fbbe4684b39101d1b148 in / 
# Thu, 22 Jul 2021 00:45:44 GMT
CMD ["bash"]
# Fri, 23 Jul 2021 12:30:11 GMT
ENV AEROSPIKE_VERSION=5.6.0.8
# Fri, 23 Jul 2021 12:30:11 GMT
ENV AEROSPIKE_SHA256=b4df1ab17f0a3cab1d5da14b7567340fe27d23e617a80b030791dd81e6afc258
# Fri, 23 Jul 2021 12:30:32 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 python3-distutils lua5.2 gettext-base libldap-dev libcurl4-openssl-dev   && wget "https://www.aerospike.com/enterprise/download/server/${AEROSPIKE_VERSION}/artifact/debian10" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Fri, 23 Jul 2021 12:30:33 GMT
COPY file:7d75174e09b209cf7f56b715636c2b8e08dd083d548e8cdc8517cabd512600b5 in /etc/aerospike/aerospike.template.conf 
# Fri, 23 Jul 2021 12:30:33 GMT
COPY file:31b6a51a1d9d91f22433472f07f6ddfe3cea3bb07f460dd69c4187bc7fd20fdf in /entrypoint.sh 
# Fri, 23 Jul 2021 12:30:33 GMT
EXPOSE 3000 3001 3002
# Fri, 23 Jul 2021 12:30:33 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Fri, 23 Jul 2021 12:30:34 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:33847f680f63fb1b343a9fc782e267b5abdbdb50d65d4b9bd2a136291d67cf75`  
		Last Modified: Thu, 22 Jul 2021 00:50:35 GMT  
		Size: 27.1 MB (27145795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b334fac9792d811fb2e9bd08a5a69f9d0a2a95d7e4d04a98ab116e7436b6e8`  
		Last Modified: Fri, 23 Jul 2021 12:31:16 GMT  
		Size: 55.3 MB (55324261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129a361e5b1e5cdd07c06fde9691a63440ef32b37f74b30553528e3e90e4bfbd`  
		Last Modified: Fri, 23 Jul 2021 12:31:08 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc5b68769cd0ac3f11e94ef061dfc4afba8fb775b9ec55b7f826a7676d933a9c`  
		Last Modified: Fri, 23 Jul 2021 12:31:08 GMT  
		Size: 908.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
