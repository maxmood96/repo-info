<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `aerospike`

-	[`aerospike:ce-5.7.0.12`](#aerospikece-57012)
-	[`aerospike:ee-5.7.0.12`](#aerospikeee-57012)
-	[`aerospike:latest`](#aerospikelatest)

## `aerospike:ce-5.7.0.12`

```console
$ docker pull aerospike@sha256:c4585d86ab6c97b1eff6048017491cad48c69d8be50d35ae69f59b7b43526082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ce-5.7.0.12` - linux; amd64

```console
$ docker pull aerospike@sha256:c26cf99aa3b0f7bcb6f984ab401ef4621578dc0020c8957b3d68e5ad15bdcb24
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81557380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36d85d53659c43b57fce6476121a595caaf5d4051823d6ffae41a53ae91a3841`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 18:57:37 GMT
ENV AEROSPIKE_VERSION=5.7.0.12
# Tue, 29 Mar 2022 18:58:00 GMT
ENV AEROSPIKE_SHA256=a763ca06c40d74aa7a1417e446aaa8f592e2367f127304495f6c9392e5b07ffd
# Tue, 29 Mar 2022 18:58:19 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 python3-distutils lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian10.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Tue, 29 Mar 2022 18:58:19 GMT
COPY file:1897c4aae07efbc61bf2d8c2c7b0dfb0990174e11cc787eac71d5adf767abaed in /etc/aerospike/aerospike.template.conf 
# Tue, 29 Mar 2022 18:58:19 GMT
COPY file:e1d47057fdb4c34c118f7ba5898161c386b475cba70907a4ae483866cf07335b in /entrypoint.sh 
# Tue, 29 Mar 2022 18:58:20 GMT
EXPOSE 3000 3001 3002
# Tue, 29 Mar 2022 18:58:20 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Tue, 29 Mar 2022 18:58:20 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8745a676328cf31adfcb48cbf3c74a94076950f6db6c89a25211241f6fe0624d`  
		Last Modified: Tue, 29 Mar 2022 18:58:58 GMT  
		Size: 54.4 MB (54403389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ce4bedb9099e1acda2351fa31d1a754e4f31a496bfbbca383d41bbd6d0971c`  
		Last Modified: Tue, 29 Mar 2022 18:58:50 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e0e3e08da1ca2f48e501e2696dd2f3690bd2f51ca2d2901749423f5ec43be1`  
		Last Modified: Tue, 29 Mar 2022 18:58:50 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:ee-5.7.0.12`

```console
$ docker pull aerospike@sha256:efbe46e36960cae378126954d2ed03ac246036e27005335be05a7c15b63bad28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ee-5.7.0.12` - linux; amd64

```console
$ docker pull aerospike@sha256:04557fdd94ae5f9876e369b6077eac948a6afd5fa84f743c21dd489e8e2e8d89
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83925102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eafc7011188330bc0d8feb15a87e3c6514577b03e4a2ff8510652d6b4aa1bf98`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 18:57:37 GMT
ENV AEROSPIKE_VERSION=5.7.0.12
# Tue, 29 Mar 2022 18:57:37 GMT
ENV AEROSPIKE_SHA256=a63a6d6d749011a3eb89ca30bb8e48dc122af9a5a87caa854c9ae6da864a1935
# Tue, 29 Mar 2022 18:57:37 GMT
ENV AS_TINI_SHA256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940
# Tue, 29 Mar 2022 18:57:56 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps wget python python3 python3-distutils lua5.2 gettext-base libldap-dev libcurl4-openssl-dev   && wget https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static -O /usr/bin/as-tini-static   && echo "$AS_TINI_SHA256 /usr/bin/as-tini-static" | sha256sum -c -   && chmod +x /usr/bin/as-tini-static   && wget "https://download.aerospike.com/artifacts/aerospike-server-enterprise/${AEROSPIKE_VERSION}/aerospike-server-enterprise-${AEROSPIKE_VERSION}-debian10.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Tue, 29 Mar 2022 18:57:57 GMT
COPY file:7d75174e09b209cf7f56b715636c2b8e08dd083d548e8cdc8517cabd512600b5 in /etc/aerospike/aerospike.template.conf 
# Tue, 29 Mar 2022 18:57:57 GMT
COPY file:31b6a51a1d9d91f22433472f07f6ddfe3cea3bb07f460dd69c4187bc7fd20fdf in /entrypoint.sh 
# Tue, 29 Mar 2022 18:57:57 GMT
EXPOSE 3000 3001 3002
# Tue, 29 Mar 2022 18:57:57 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 29 Mar 2022 18:57:57 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173ee40f2c01cb9d5297ea1226f5bf63e85d5ccf2558dc98dd6d34c995ad526e`  
		Last Modified: Tue, 29 Mar 2022 18:58:40 GMT  
		Size: 56.8 MB (56771050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0244416042e5c57613770f93c8e195e14dfaa14c7e311559878c4ef393d06d79`  
		Last Modified: Tue, 29 Mar 2022 18:58:32 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b3f5905d21f685d73db4818d30842579e29a1c3d406deb353f397c5ca300bb5`  
		Last Modified: Tue, 29 Mar 2022 18:58:32 GMT  
		Size: 908.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:latest`

```console
$ docker pull aerospike@sha256:efbe46e36960cae378126954d2ed03ac246036e27005335be05a7c15b63bad28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:latest` - linux; amd64

```console
$ docker pull aerospike@sha256:04557fdd94ae5f9876e369b6077eac948a6afd5fa84f743c21dd489e8e2e8d89
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83925102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eafc7011188330bc0d8feb15a87e3c6514577b03e4a2ff8510652d6b4aa1bf98`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 18:57:37 GMT
ENV AEROSPIKE_VERSION=5.7.0.12
# Tue, 29 Mar 2022 18:57:37 GMT
ENV AEROSPIKE_SHA256=a63a6d6d749011a3eb89ca30bb8e48dc122af9a5a87caa854c9ae6da864a1935
# Tue, 29 Mar 2022 18:57:37 GMT
ENV AS_TINI_SHA256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940
# Tue, 29 Mar 2022 18:57:56 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps wget python python3 python3-distutils lua5.2 gettext-base libldap-dev libcurl4-openssl-dev   && wget https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static -O /usr/bin/as-tini-static   && echo "$AS_TINI_SHA256 /usr/bin/as-tini-static" | sha256sum -c -   && chmod +x /usr/bin/as-tini-static   && wget "https://download.aerospike.com/artifacts/aerospike-server-enterprise/${AEROSPIKE_VERSION}/aerospike-server-enterprise-${AEROSPIKE_VERSION}-debian10.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Tue, 29 Mar 2022 18:57:57 GMT
COPY file:7d75174e09b209cf7f56b715636c2b8e08dd083d548e8cdc8517cabd512600b5 in /etc/aerospike/aerospike.template.conf 
# Tue, 29 Mar 2022 18:57:57 GMT
COPY file:31b6a51a1d9d91f22433472f07f6ddfe3cea3bb07f460dd69c4187bc7fd20fdf in /entrypoint.sh 
# Tue, 29 Mar 2022 18:57:57 GMT
EXPOSE 3000 3001 3002
# Tue, 29 Mar 2022 18:57:57 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 29 Mar 2022 18:57:57 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173ee40f2c01cb9d5297ea1226f5bf63e85d5ccf2558dc98dd6d34c995ad526e`  
		Last Modified: Tue, 29 Mar 2022 18:58:40 GMT  
		Size: 56.8 MB (56771050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0244416042e5c57613770f93c8e195e14dfaa14c7e311559878c4ef393d06d79`  
		Last Modified: Tue, 29 Mar 2022 18:58:32 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b3f5905d21f685d73db4818d30842579e29a1c3d406deb353f397c5ca300bb5`  
		Last Modified: Tue, 29 Mar 2022 18:58:32 GMT  
		Size: 908.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
