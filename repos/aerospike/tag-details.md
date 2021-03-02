<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `aerospike`

-	[`aerospike:5.3.0.10`](#aerospike53010)
-	[`aerospike:5.4.0.5`](#aerospike5405)
-	[`aerospike:5.5.0.3`](#aerospike5503)
-	[`aerospike:latest`](#aerospikelatest)

## `aerospike:5.3.0.10`

```console
$ docker pull aerospike@sha256:116fd9d015830922ca3572040b3ddda4bcc4458e09c99cbded3acbae0ab33b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:5.3.0.10` - linux; amd64

```console
$ docker pull aerospike@sha256:e48e215f93a14ed8c3b1addc6f0e36fb8c1ee7594554fb24e7cd9eb204f4bb76
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74713120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da292fff8ce9e0842f32f40cfb886a2ca56dcd803787a6e3209b58ca51e7d3b4`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:30 GMT
ADD file:da0c935ddc86ca9e44bdd5f61b46c7b43a115ee4bc356324265a7ad6323f61ae in / 
# Tue, 09 Feb 2021 02:23:30 GMT
CMD ["bash"]
# Tue, 02 Mar 2021 22:19:39 GMT
ENV AEROSPIKE_VERSION=5.3.0.10
# Tue, 02 Mar 2021 22:19:39 GMT
ENV AEROSPIKE_SHA256=d05e9db2936fda4e29fdd6bd3115f98c96f3c3eda22b1328f735869520b34307
# Tue, 02 Mar 2021 22:20:02 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Tue, 02 Mar 2021 22:20:03 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Tue, 02 Mar 2021 22:20:03 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Tue, 02 Mar 2021 22:20:03 GMT
EXPOSE 3000 3001 3002 3003
# Tue, 02 Mar 2021 22:20:03 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Tue, 02 Mar 2021 22:20:04 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:cae7303ade7f17f84fe86b2a44880e9725cf7d6dcd17f79485360712b6af6dcd`  
		Last Modified: Tue, 09 Feb 2021 02:29:36 GMT  
		Size: 22.5 MB (22528600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be36128968b68aed67171d4c8945e855985bda11f38e85c659851de1fcc49ccc`  
		Last Modified: Tue, 02 Mar 2021 22:21:22 GMT  
		Size: 52.2 MB (52182469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2be2dee3145dadccb9e8d6e3c914eb4beef18e4d2abeff5e8a12f4053576e2dd`  
		Last Modified: Tue, 02 Mar 2021 22:21:12 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae781e4279dbd74d579123a1ab81b973bfedae440c448dada6a73e63da38779`  
		Last Modified: Tue, 02 Mar 2021 22:21:12 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:5.4.0.5`

```console
$ docker pull aerospike@sha256:dbbfaf8783a14cf5b242cda44d837b7640334174a4460b5daf0e59038e284d07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:5.4.0.5` - linux; amd64

```console
$ docker pull aerospike@sha256:44cc7895f7cd3a1bf7f3a8758ce2d4fb721ff50f3494d5cdcbf6b2ce88f35894
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74731080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb02ab20ee8f830a06d2c65826c13b44299190aa4118f18ca013fe6eb208f55`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:30 GMT
ADD file:da0c935ddc86ca9e44bdd5f61b46c7b43a115ee4bc356324265a7ad6323f61ae in / 
# Tue, 09 Feb 2021 02:23:30 GMT
CMD ["bash"]
# Tue, 02 Mar 2021 22:20:08 GMT
ENV AEROSPIKE_VERSION=5.4.0.5
# Tue, 02 Mar 2021 22:20:08 GMT
ENV AEROSPIKE_SHA256=a30f09784dfa4dda36af633210b43cda493663d2faedac87b8b27aa4f60d0231
# Tue, 02 Mar 2021 22:20:32 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Tue, 02 Mar 2021 22:20:32 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Tue, 02 Mar 2021 22:20:32 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Tue, 02 Mar 2021 22:20:33 GMT
EXPOSE 3000 3001 3002 3003
# Tue, 02 Mar 2021 22:20:33 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Tue, 02 Mar 2021 22:20:33 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:cae7303ade7f17f84fe86b2a44880e9725cf7d6dcd17f79485360712b6af6dcd`  
		Last Modified: Tue, 09 Feb 2021 02:29:36 GMT  
		Size: 22.5 MB (22528600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120bf4b7accbc89bca328fe668795fc88bba3f9bc76a7099d581f13e409dda2f`  
		Last Modified: Tue, 02 Mar 2021 22:21:35 GMT  
		Size: 52.2 MB (52200428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6370585f8abe8572d763effdb8c889f8cae84fefb40658918d95cf8c62e49f86`  
		Last Modified: Tue, 02 Mar 2021 22:21:26 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516ccfdb786cfd6f4c0388f9ddf6371e95f453223379d11babc19a795f96420f`  
		Last Modified: Tue, 02 Mar 2021 22:21:26 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:5.5.0.3`

```console
$ docker pull aerospike@sha256:7741e3d181a1c76018ae5e07219ca5abc07f795fe7404eeeaf9fd0765912c528
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:5.5.0.3` - linux; amd64

```console
$ docker pull aerospike@sha256:ef66fc69fa2f10b7371c34e3c27027e856c52ee5017a07c6821c78b835e6aea2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74771022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280787e9c7ca9755e5402df9fc8c8ccad132e263f8100a455397bf15a84156a0`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:30 GMT
ADD file:da0c935ddc86ca9e44bdd5f61b46c7b43a115ee4bc356324265a7ad6323f61ae in / 
# Tue, 09 Feb 2021 02:23:30 GMT
CMD ["bash"]
# Tue, 02 Mar 2021 22:20:38 GMT
ENV AEROSPIKE_VERSION=5.5.0.3
# Tue, 02 Mar 2021 22:20:38 GMT
ENV AEROSPIKE_SHA256=5649c59750042c8926af6ea2120a9ce6de008e9e4fede1329735b32a82f6dec2
# Tue, 02 Mar 2021 22:21:01 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Tue, 02 Mar 2021 22:21:01 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Tue, 02 Mar 2021 22:21:01 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Tue, 02 Mar 2021 22:21:01 GMT
EXPOSE 3000 3001 3002 3003
# Tue, 02 Mar 2021 22:21:02 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Tue, 02 Mar 2021 22:21:02 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:cae7303ade7f17f84fe86b2a44880e9725cf7d6dcd17f79485360712b6af6dcd`  
		Last Modified: Tue, 09 Feb 2021 02:29:36 GMT  
		Size: 22.5 MB (22528600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aae733051beaa65eeebe04ecd8db6487ee3b6489e1a6e099ebf591a2d18f8810`  
		Last Modified: Tue, 02 Mar 2021 22:21:49 GMT  
		Size: 52.2 MB (52240370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb979da4fce90ce00813049f0a3460ab09bc577c34c35e399f322e33752d7ea`  
		Last Modified: Tue, 02 Mar 2021 22:21:39 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85646e48fe8f2cfcbb8f2bacdc9f7aa0db87c409ae42c8b437c4a9f1e5313956`  
		Last Modified: Tue, 02 Mar 2021 22:21:39 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:latest`

```console
$ docker pull aerospike@sha256:7741e3d181a1c76018ae5e07219ca5abc07f795fe7404eeeaf9fd0765912c528
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:latest` - linux; amd64

```console
$ docker pull aerospike@sha256:ef66fc69fa2f10b7371c34e3c27027e856c52ee5017a07c6821c78b835e6aea2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74771022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280787e9c7ca9755e5402df9fc8c8ccad132e263f8100a455397bf15a84156a0`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:30 GMT
ADD file:da0c935ddc86ca9e44bdd5f61b46c7b43a115ee4bc356324265a7ad6323f61ae in / 
# Tue, 09 Feb 2021 02:23:30 GMT
CMD ["bash"]
# Tue, 02 Mar 2021 22:20:38 GMT
ENV AEROSPIKE_VERSION=5.5.0.3
# Tue, 02 Mar 2021 22:20:38 GMT
ENV AEROSPIKE_SHA256=5649c59750042c8926af6ea2120a9ce6de008e9e4fede1329735b32a82f6dec2
# Tue, 02 Mar 2021 22:21:01 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Tue, 02 Mar 2021 22:21:01 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Tue, 02 Mar 2021 22:21:01 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Tue, 02 Mar 2021 22:21:01 GMT
EXPOSE 3000 3001 3002 3003
# Tue, 02 Mar 2021 22:21:02 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Tue, 02 Mar 2021 22:21:02 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:cae7303ade7f17f84fe86b2a44880e9725cf7d6dcd17f79485360712b6af6dcd`  
		Last Modified: Tue, 09 Feb 2021 02:29:36 GMT  
		Size: 22.5 MB (22528600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aae733051beaa65eeebe04ecd8db6487ee3b6489e1a6e099ebf591a2d18f8810`  
		Last Modified: Tue, 02 Mar 2021 22:21:49 GMT  
		Size: 52.2 MB (52240370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb979da4fce90ce00813049f0a3460ab09bc577c34c35e399f322e33752d7ea`  
		Last Modified: Tue, 02 Mar 2021 22:21:39 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85646e48fe8f2cfcbb8f2bacdc9f7aa0db87c409ae42c8b437c4a9f1e5313956`  
		Last Modified: Tue, 02 Mar 2021 22:21:39 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
