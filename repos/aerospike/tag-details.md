<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `aerospike`

-	[`aerospike:ce-5.6.0.9`](#aerospikece-5609)
-	[`aerospike:ee-5.6.0.9`](#aerospikeee-5609)

## `aerospike:ce-5.6.0.9`

```console
$ docker pull aerospike@sha256:80ac48b37f5b2363ccf6ab4155b568fd399a21b6042f6d714a7d0dfc7b1a05f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ce-5.6.0.9` - linux; amd64

```console
$ docker pull aerospike@sha256:267e32a909f023209da3db98bf59ff25b2c1ab6ae28415e362f31d4a7123c159
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.6 MB (80606320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a61f91776c75f993da0d663f78646e5eba101d01c0ae489d1f1b0350cd178b01`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 17 Aug 2021 01:24:06 GMT
ADD file:87b4e60fe3af680c6815448374365a44e9ea461bc8ade2960b4639c25aed3ba9 in / 
# Tue, 17 Aug 2021 01:24:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:16:39 GMT
ENV AEROSPIKE_VERSION=5.6.0.9
# Tue, 17 Aug 2021 09:17:15 GMT
ENV AEROSPIKE_SHA256=82b15902420752273e22405d929e43a7062e9c84b604e2c1e9f27d26c8ae0aad
# Tue, 17 Aug 2021 09:17:43 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 python3-distutils lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian10.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Tue, 17 Aug 2021 09:17:44 GMT
COPY file:1897c4aae07efbc61bf2d8c2c7b0dfb0990174e11cc787eac71d5adf767abaed in /etc/aerospike/aerospike.template.conf 
# Tue, 17 Aug 2021 09:17:44 GMT
COPY file:e1d47057fdb4c34c118f7ba5898161c386b475cba70907a4ae483866cf07335b in /entrypoint.sh 
# Tue, 17 Aug 2021 09:17:45 GMT
EXPOSE 3000 3001 3002
# Tue, 17 Aug 2021 09:17:45 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Tue, 17 Aug 2021 09:17:45 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:e1acddbe380c63f0de4b77d3f287b7c81cd9d89563a230692378126b46ea6546`  
		Last Modified: Tue, 17 Aug 2021 01:30:21 GMT  
		Size: 27.1 MB (27145985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95acd7bb4a98720410868aa4b5105cf54ca01aa6550160652382df0a3910f3c5`  
		Last Modified: Tue, 17 Aug 2021 09:18:24 GMT  
		Size: 53.5 MB (53458313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781a3ca2098f290c6305cb8c2534a6781ab348030458a4980d7bdbf496f9974c`  
		Last Modified: Tue, 17 Aug 2021 09:18:15 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847167a29a6ec62cb9a7a1e9612ba89ebd2ad40e88efd91330abdaf144449116`  
		Last Modified: Tue, 17 Aug 2021 09:18:15 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:ee-5.6.0.9`

```console
$ docker pull aerospike@sha256:25f33ab5d98f5bbb744566ee251c0f83cb016db1a2090078694c82ede73bb8e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ee-5.6.0.9` - linux; amd64

```console
$ docker pull aerospike@sha256:3be34989fd43b1c967199091aa16ee9f39a5154aca23e94d99353dd8be2c8c31
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82472369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d210595632e090f5c03744d01d15ae8a6a44882515ee8b3a3c31b35ab7a621b`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 17 Aug 2021 01:24:06 GMT
ADD file:87b4e60fe3af680c6815448374365a44e9ea461bc8ade2960b4639c25aed3ba9 in / 
# Tue, 17 Aug 2021 01:24:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:16:39 GMT
ENV AEROSPIKE_VERSION=5.6.0.9
# Tue, 17 Aug 2021 09:16:39 GMT
ENV AEROSPIKE_SHA256=c7b16a194bc6a025b7f97f962a4102da255c38bdf99ff59bea15349be3bd02cb
# Tue, 17 Aug 2021 09:17:07 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 python3-distutils lua5.2 gettext-base libldap-dev libcurl4-openssl-dev   && wget "https://www.aerospike.com/enterprise/download/server/${AEROSPIKE_VERSION}/artifact/debian10" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Tue, 17 Aug 2021 09:17:07 GMT
COPY file:7d75174e09b209cf7f56b715636c2b8e08dd083d548e8cdc8517cabd512600b5 in /etc/aerospike/aerospike.template.conf 
# Tue, 17 Aug 2021 09:17:08 GMT
COPY file:31b6a51a1d9d91f22433472f07f6ddfe3cea3bb07f460dd69c4187bc7fd20fdf in /entrypoint.sh 
# Tue, 17 Aug 2021 09:17:08 GMT
EXPOSE 3000 3001 3002
# Tue, 17 Aug 2021 09:17:08 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Tue, 17 Aug 2021 09:17:08 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:e1acddbe380c63f0de4b77d3f287b7c81cd9d89563a230692378126b46ea6546`  
		Last Modified: Tue, 17 Aug 2021 01:30:21 GMT  
		Size: 27.1 MB (27145985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26898e6fed654ad6c4d799db16b4ce7a029dfa38a2ae4696f7c17eae13315c2`  
		Last Modified: Tue, 17 Aug 2021 09:18:07 GMT  
		Size: 55.3 MB (55324299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e94e9f6e80548e3b40b9640ae88e7a89c09a66634e99ed53692bfff97d1b82e`  
		Last Modified: Tue, 17 Aug 2021 09:17:57 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56cee5a41f2363c602d17f9d8e46a97f792addbd4aad1d1da8f3e980a40066f4`  
		Last Modified: Tue, 17 Aug 2021 09:17:58 GMT  
		Size: 910.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
