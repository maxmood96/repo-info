<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `aerospike`

-	[`aerospike:5.3.0.10`](#aerospike53010)
-	[`aerospike:5.4.0.5`](#aerospike5405)
-	[`aerospike:5.5.0.3`](#aerospike5503)
-	[`aerospike:latest`](#aerospikelatest)

## `aerospike:5.3.0.10`

```console
$ docker pull aerospike@sha256:cdf9a65c9ae4e82115c752ac67d0da3382ea4d629f290ada40db99c0e466bb2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:5.3.0.10` - linux; amd64

```console
$ docker pull aerospike@sha256:0dd9272bdeffd52e8a95907d50bdae015d94129fb74e319211b9be1430604d6c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74717384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff5528fa36259b9d56bc9af3ef09f6c273e3541281c517a313dcd3daa7ad42c`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Fri, 26 Mar 2021 15:23:32 GMT
ADD file:72268d05e43fe7fe347fba8d003dbe9926a595c116e761cf3997af09cfa0ee19 in / 
# Fri, 26 Mar 2021 15:23:32 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 05:37:18 GMT
ENV AEROSPIKE_VERSION=5.3.0.10
# Sat, 27 Mar 2021 05:37:18 GMT
ENV AEROSPIKE_SHA256=d05e9db2936fda4e29fdd6bd3115f98c96f3c3eda22b1328f735869520b34307
# Sat, 27 Mar 2021 05:37:41 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Sat, 27 Mar 2021 05:37:42 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Sat, 27 Mar 2021 05:37:42 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Sat, 27 Mar 2021 05:37:42 GMT
EXPOSE 3000 3001 3002 3003
# Sat, 27 Mar 2021 05:37:43 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Sat, 27 Mar 2021 05:37:43 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:b5887238bf65fc2f40fdd004509b96300faa112cc64eb2865a09895474269ee7`  
		Last Modified: Fri, 26 Mar 2021 15:32:49 GMT  
		Size: 22.5 MB (22528402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d359e5db33942275c8d2cf00d136fd4b9aa4d3c867c75d0bebbea7c26526444`  
		Last Modified: Sat, 27 Mar 2021 05:39:02 GMT  
		Size: 52.2 MB (52186928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c46a487912204f03e7dee5f687731e00f92545d2af55e00608233921e83ee6`  
		Last Modified: Sat, 27 Mar 2021 05:38:52 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5828bb650e96835dc36e66a603d6bd50b48c0f0159d8fa4b004bcbe6792799f0`  
		Last Modified: Sat, 27 Mar 2021 05:38:52 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:5.4.0.5`

```console
$ docker pull aerospike@sha256:aaa533d143ee85ec5322b63b2c9577d6f116568ee462f303eb44e8abf1fd5797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:5.4.0.5` - linux; amd64

```console
$ docker pull aerospike@sha256:0930d9b4049456485d75ac42ce43931bd6bcad12b751d62f933c97ca7ad7d092
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74737747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ea56bb6c99ffd8b5817530cc3ca80858b58f2468b75a2f07058d1de728c50e`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Fri, 26 Mar 2021 15:23:32 GMT
ADD file:72268d05e43fe7fe347fba8d003dbe9926a595c116e761cf3997af09cfa0ee19 in / 
# Fri, 26 Mar 2021 15:23:32 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 05:37:48 GMT
ENV AEROSPIKE_VERSION=5.4.0.5
# Sat, 27 Mar 2021 05:37:48 GMT
ENV AEROSPIKE_SHA256=a30f09784dfa4dda36af633210b43cda493663d2faedac87b8b27aa4f60d0231
# Sat, 27 Mar 2021 05:38:08 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Sat, 27 Mar 2021 05:38:09 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Sat, 27 Mar 2021 05:38:09 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Sat, 27 Mar 2021 05:38:09 GMT
EXPOSE 3000 3001 3002 3003
# Sat, 27 Mar 2021 05:38:10 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Sat, 27 Mar 2021 05:38:10 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:b5887238bf65fc2f40fdd004509b96300faa112cc64eb2865a09895474269ee7`  
		Last Modified: Fri, 26 Mar 2021 15:32:49 GMT  
		Size: 22.5 MB (22528402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78934316c6cf86a5ae534cdb23f38efc23d75b6ffc68efe4278fa4d0d5ba78f2`  
		Last Modified: Sat, 27 Mar 2021 05:39:23 GMT  
		Size: 52.2 MB (52207289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ea42c69655ccd8159a3e11822f275309ec9a4772b7729872c822fb13f01eee`  
		Last Modified: Sat, 27 Mar 2021 05:39:15 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a489669953bacaa0a43045389776228b17a38624bc978c0f5056c698d75d9e6f`  
		Last Modified: Sat, 27 Mar 2021 05:39:15 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:5.5.0.3`

```console
$ docker pull aerospike@sha256:146c6f2997adafc59050fdc70bcaa431a8aabbd2bad0a10077a9a8e30e7b1c90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:5.5.0.3` - linux; amd64

```console
$ docker pull aerospike@sha256:781f0a9caa444fa29c6446b8eee230654514f2b8ceb471137112f23544ca6da9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74776003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff34646d991244cf3646a7f347344844ed7e9f2d4c9f9b83b00c922cc3b745d6`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Fri, 26 Mar 2021 15:23:32 GMT
ADD file:72268d05e43fe7fe347fba8d003dbe9926a595c116e761cf3997af09cfa0ee19 in / 
# Fri, 26 Mar 2021 15:23:32 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 05:38:14 GMT
ENV AEROSPIKE_VERSION=5.5.0.3
# Sat, 27 Mar 2021 05:38:14 GMT
ENV AEROSPIKE_SHA256=5649c59750042c8926af6ea2120a9ce6de008e9e4fede1329735b32a82f6dec2
# Sat, 27 Mar 2021 05:38:36 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Sat, 27 Mar 2021 05:38:37 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Sat, 27 Mar 2021 05:38:37 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Sat, 27 Mar 2021 05:38:37 GMT
EXPOSE 3000 3001 3002 3003
# Sat, 27 Mar 2021 05:38:38 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Sat, 27 Mar 2021 05:38:38 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:b5887238bf65fc2f40fdd004509b96300faa112cc64eb2865a09895474269ee7`  
		Last Modified: Fri, 26 Mar 2021 15:32:49 GMT  
		Size: 22.5 MB (22528402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d898db50487d764d1a466b828ce00d8a04683e88e2411ddbd04d6be915fad43b`  
		Last Modified: Sat, 27 Mar 2021 05:39:41 GMT  
		Size: 52.2 MB (52245548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f44b1e577c271492e7f214ec0a663190c2dd7091d71cc2110d3abc14f21300ff`  
		Last Modified: Sat, 27 Mar 2021 05:39:31 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9151f4d4a3803b1d6ed08f1835b63c7c001d68c6f43c16d44c14309ff38619c2`  
		Last Modified: Sat, 27 Mar 2021 05:39:31 GMT  
		Size: 900.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:latest`

```console
$ docker pull aerospike@sha256:146c6f2997adafc59050fdc70bcaa431a8aabbd2bad0a10077a9a8e30e7b1c90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:latest` - linux; amd64

```console
$ docker pull aerospike@sha256:781f0a9caa444fa29c6446b8eee230654514f2b8ceb471137112f23544ca6da9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74776003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff34646d991244cf3646a7f347344844ed7e9f2d4c9f9b83b00c922cc3b745d6`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Fri, 26 Mar 2021 15:23:32 GMT
ADD file:72268d05e43fe7fe347fba8d003dbe9926a595c116e761cf3997af09cfa0ee19 in / 
# Fri, 26 Mar 2021 15:23:32 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 05:38:14 GMT
ENV AEROSPIKE_VERSION=5.5.0.3
# Sat, 27 Mar 2021 05:38:14 GMT
ENV AEROSPIKE_SHA256=5649c59750042c8926af6ea2120a9ce6de008e9e4fede1329735b32a82f6dec2
# Sat, 27 Mar 2021 05:38:36 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Sat, 27 Mar 2021 05:38:37 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Sat, 27 Mar 2021 05:38:37 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Sat, 27 Mar 2021 05:38:37 GMT
EXPOSE 3000 3001 3002 3003
# Sat, 27 Mar 2021 05:38:38 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Sat, 27 Mar 2021 05:38:38 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:b5887238bf65fc2f40fdd004509b96300faa112cc64eb2865a09895474269ee7`  
		Last Modified: Fri, 26 Mar 2021 15:32:49 GMT  
		Size: 22.5 MB (22528402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d898db50487d764d1a466b828ce00d8a04683e88e2411ddbd04d6be915fad43b`  
		Last Modified: Sat, 27 Mar 2021 05:39:41 GMT  
		Size: 52.2 MB (52245548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f44b1e577c271492e7f214ec0a663190c2dd7091d71cc2110d3abc14f21300ff`  
		Last Modified: Sat, 27 Mar 2021 05:39:31 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9151f4d4a3803b1d6ed08f1835b63c7c001d68c6f43c16d44c14309ff38619c2`  
		Last Modified: Sat, 27 Mar 2021 05:39:31 GMT  
		Size: 900.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
