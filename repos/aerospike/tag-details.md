<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `aerospike`

-	[`aerospike:5.0.0.18`](#aerospike50018)
-	[`aerospike:5.1.0.15`](#aerospike51015)
-	[`aerospike:5.2.0.7`](#aerospike5207)
-	[`aerospike:latest`](#aerospikelatest)

## `aerospike:5.0.0.18`

```console
$ docker pull aerospike@sha256:b9c9e73c4b558e51ca19326b4438b338609d1e5029e63517c20e01e2f6357ae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:5.0.0.18` - linux; amd64

```console
$ docker pull aerospike@sha256:4b58e8dd149c2e16dd07964e623ef70d930aa55769f6ca6685bfc8f852cefc81
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59777208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ca3b890a3f60928398ac9473f330fcf274ed1cc11ee3b767a2e0df80caa68d9`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 13 Oct 2020 01:44:45 GMT
ADD file:4453535d387fcb17ead2026c72c05444e7558aa4736e3c0cdfb87cf20eaa5a9f in / 
# Tue, 13 Oct 2020 01:44:45 GMT
CMD ["bash"]
# Thu, 12 Nov 2020 00:21:47 GMT
ENV AEROSPIKE_VERSION=5.0.0.18
# Thu, 12 Nov 2020 00:21:47 GMT
ENV AEROSPIKE_SHA256=108cbf5c90542a2760549a934a71f6267899c6589b1e21bf8a5d79ac9665ff18
# Thu, 12 Nov 2020 00:22:05 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Thu, 12 Nov 2020 00:22:05 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Thu, 12 Nov 2020 00:22:06 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Thu, 12 Nov 2020 00:22:06 GMT
EXPOSE 3000 3001 3002 3003
# Thu, 12 Nov 2020 00:22:06 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Thu, 12 Nov 2020 00:22:06 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:babf97a3f00ae0a4d59c1a0f88918d8f7aa0f0758380258b2016f0cd17e97202`  
		Last Modified: Tue, 13 Oct 2020 01:51:03 GMT  
		Size: 22.5 MB (22522093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d32e2eaa4748c942114eff667b7f9c525e6f76f0c6be46c7deebef4b4768a9`  
		Last Modified: Thu, 12 Nov 2020 00:23:12 GMT  
		Size: 37.3 MB (37253065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc926ced757ec5f80467ae833b3dd17a50f91a62b434439cc0a946433c1f26ab`  
		Last Modified: Thu, 12 Nov 2020 00:23:06 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7047b7a2794e2fc1d386b695daa268941aa9ac3656a18e35a44bf9e71ae5dd6b`  
		Last Modified: Thu, 12 Nov 2020 00:23:07 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:5.1.0.15`

```console
$ docker pull aerospike@sha256:b8b2571fce1b9d098660938f3135e63fa8471b6c6a59a580b807f06cfef885c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:5.1.0.15` - linux; amd64

```console
$ docker pull aerospike@sha256:3b939f7cd1854a9c2d63c90e3a3ff9af091293730a89e863d9243594bae13813
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67210990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a5241c6abbdd50b82609cdcf059fa4f375d7def750adb0ff5297935ba0b3169`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 13 Oct 2020 01:44:45 GMT
ADD file:4453535d387fcb17ead2026c72c05444e7558aa4736e3c0cdfb87cf20eaa5a9f in / 
# Tue, 13 Oct 2020 01:44:45 GMT
CMD ["bash"]
# Thu, 12 Nov 2020 00:22:12 GMT
ENV AEROSPIKE_VERSION=5.1.0.15
# Thu, 12 Nov 2020 00:22:12 GMT
ENV AEROSPIKE_SHA256=e356aa2b6cc4e93d6030f1f8f5c598a8c2a17f00723e82d89c77dc9266ed67bc
# Thu, 12 Nov 2020 00:22:31 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Thu, 12 Nov 2020 00:22:31 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Thu, 12 Nov 2020 00:22:31 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Thu, 12 Nov 2020 00:22:31 GMT
EXPOSE 3000 3001 3002 3003
# Thu, 12 Nov 2020 00:22:32 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Thu, 12 Nov 2020 00:22:32 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:babf97a3f00ae0a4d59c1a0f88918d8f7aa0f0758380258b2016f0cd17e97202`  
		Last Modified: Tue, 13 Oct 2020 01:51:03 GMT  
		Size: 22.5 MB (22522093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848e9ec7443caec646b5b8357a31391f400de85a71b8150bf585b92dd97dc032`  
		Last Modified: Thu, 12 Nov 2020 00:23:29 GMT  
		Size: 44.7 MB (44686848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d396cd0d5c85c7e847840d6c4740f06a4dfa64ee5b06396c7a5af4357896281`  
		Last Modified: Thu, 12 Nov 2020 00:23:22 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:987d8827b6c00aa12c1269380157576d2f900ced4f9100c644a5c0da1081f8f7`  
		Last Modified: Thu, 12 Nov 2020 00:23:21 GMT  
		Size: 898.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:5.2.0.7`

```console
$ docker pull aerospike@sha256:a5a4cb866b7bc2b0b4dfc85c19f2f7d49d1d86388f66cf42e87e6547e96c5e64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:5.2.0.7` - linux; amd64

```console
$ docker pull aerospike@sha256:84414869abbaae1e66a22bd4478eee6b2aa1bfc4540ea20dbb912c24dcd10e87
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67127935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67e6cf3b0f3de0472880a33ccbf8e3a2533e45174939e6461585205384c6c071`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 13 Oct 2020 01:44:45 GMT
ADD file:4453535d387fcb17ead2026c72c05444e7558aa4736e3c0cdfb87cf20eaa5a9f in / 
# Tue, 13 Oct 2020 01:44:45 GMT
CMD ["bash"]
# Thu, 12 Nov 2020 00:22:38 GMT
ENV AEROSPIKE_VERSION=5.2.0.7
# Thu, 12 Nov 2020 00:22:38 GMT
ENV AEROSPIKE_SHA256=5f64b516be56f16a708991785d9525c18dc16f73418070738c3e5dd3dcae7ea8
# Thu, 12 Nov 2020 00:22:56 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Thu, 12 Nov 2020 00:22:56 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Thu, 12 Nov 2020 00:22:57 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Thu, 12 Nov 2020 00:22:57 GMT
EXPOSE 3000 3001 3002 3003
# Thu, 12 Nov 2020 00:22:57 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Thu, 12 Nov 2020 00:22:57 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:babf97a3f00ae0a4d59c1a0f88918d8f7aa0f0758380258b2016f0cd17e97202`  
		Last Modified: Tue, 13 Oct 2020 01:51:03 GMT  
		Size: 22.5 MB (22522093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c048ad2573b82740eb3c6148d30f5855ca4af9a8f46e79133b9c8392dcd6b8fd`  
		Last Modified: Thu, 12 Nov 2020 00:23:40 GMT  
		Size: 44.6 MB (44603789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25098bd0315605329b0b31c129e5a045b79146e46bd472c21424c7e68f78d467`  
		Last Modified: Thu, 12 Nov 2020 00:23:34 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7953d7b8f45451fda8d6ff459599b89907213b37260bc61de7cec9ba8bf23b3f`  
		Last Modified: Thu, 12 Nov 2020 00:23:33 GMT  
		Size: 898.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:latest`

```console
$ docker pull aerospike@sha256:a5a4cb866b7bc2b0b4dfc85c19f2f7d49d1d86388f66cf42e87e6547e96c5e64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:latest` - linux; amd64

```console
$ docker pull aerospike@sha256:84414869abbaae1e66a22bd4478eee6b2aa1bfc4540ea20dbb912c24dcd10e87
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67127935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67e6cf3b0f3de0472880a33ccbf8e3a2533e45174939e6461585205384c6c071`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 13 Oct 2020 01:44:45 GMT
ADD file:4453535d387fcb17ead2026c72c05444e7558aa4736e3c0cdfb87cf20eaa5a9f in / 
# Tue, 13 Oct 2020 01:44:45 GMT
CMD ["bash"]
# Thu, 12 Nov 2020 00:22:38 GMT
ENV AEROSPIKE_VERSION=5.2.0.7
# Thu, 12 Nov 2020 00:22:38 GMT
ENV AEROSPIKE_SHA256=5f64b516be56f16a708991785d9525c18dc16f73418070738c3e5dd3dcae7ea8
# Thu, 12 Nov 2020 00:22:56 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Thu, 12 Nov 2020 00:22:56 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Thu, 12 Nov 2020 00:22:57 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Thu, 12 Nov 2020 00:22:57 GMT
EXPOSE 3000 3001 3002 3003
# Thu, 12 Nov 2020 00:22:57 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Thu, 12 Nov 2020 00:22:57 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:babf97a3f00ae0a4d59c1a0f88918d8f7aa0f0758380258b2016f0cd17e97202`  
		Last Modified: Tue, 13 Oct 2020 01:51:03 GMT  
		Size: 22.5 MB (22522093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c048ad2573b82740eb3c6148d30f5855ca4af9a8f46e79133b9c8392dcd6b8fd`  
		Last Modified: Thu, 12 Nov 2020 00:23:40 GMT  
		Size: 44.6 MB (44603789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25098bd0315605329b0b31c129e5a045b79146e46bd472c21424c7e68f78d467`  
		Last Modified: Thu, 12 Nov 2020 00:23:34 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7953d7b8f45451fda8d6ff459599b89907213b37260bc61de7cec9ba8bf23b3f`  
		Last Modified: Thu, 12 Nov 2020 00:23:33 GMT  
		Size: 898.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
