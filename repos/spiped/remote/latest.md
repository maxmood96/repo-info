## `spiped:latest`

```console
$ docker pull spiped@sha256:c377e8d36669e684b0d0101cd0fabae0a50ba166d79822c9de411d75f42b55f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `spiped:latest` - linux; amd64

```console
$ docker pull spiped@sha256:fea99c454ce0fbe794959c712b9aa8211a59ec36d96ba4ec47e615983a02df9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36828407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61044b76967f0bfbd214c3f0c337a70e34bd5e0113b94ee6aee969afe8ae0c9b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Fri, 29 Aug 2025 17:20:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
VOLUME [/spiped]
# Fri, 29 Aug 2025 17:20:00 GMT
WORKDIR /spiped
# Fri, 29 Aug 2025 17:20:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 17:20:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc238e6158ba23ca3c78f09a916e5b8debcb8fc98435ef72ed1372e4a10d36f0`  
		Last Modified: Tue, 30 Sep 2025 00:09:33 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91631db32462bfbb6f6adbfce206c84ea557ef848ce2db5acbc296919b1e2fb8`  
		Last Modified: Tue, 30 Sep 2025 00:09:33 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bfab92e44961e7c708e76600cd2a58da46309cb1585752de3faf3cf12144b9b`  
		Last Modified: Tue, 30 Sep 2025 00:09:34 GMT  
		Size: 7.0 MB (7048278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6723c6fe89d1ee4486ae7f1aba339a847174340058a9aafba610b8f5d08c392a`  
		Last Modified: Tue, 30 Sep 2025 00:09:34 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638bc283d4e51af75c91b14cfc4325a4b783724ecdd9ac3d936db49437b45069`  
		Last Modified: Tue, 30 Sep 2025 00:09:34 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:9c5b20ad1230caec7f7f817835a32a8e84c0749bb0cec2f1338c9f94d9cafdf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a39fc5ab26c741f2fadea946a1e3f5f8d5f57b2c46254f39a4cf3dec01016afc`

```dockerfile
```

-	Layers:
	-	`sha256:6162c674076105e040975f2f9084082ad1c95d3491863ccfc1a758ad44af0f88`  
		Last Modified: Tue, 30 Sep 2025 01:04:20 GMT  
		Size: 3.6 MB (3626078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e718aeb59e0ddcdc8ae0d260d22d1e426d5f84484cbe07357ab801c3c2ae2ac`  
		Last Modified: Tue, 30 Sep 2025 01:04:20 GMT  
		Size: 15.0 KB (15025 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v5

```console
$ docker pull spiped@sha256:0ae5335373d50afd2ebe6afcfa6f6be07e82a19bded4d420d96db3555cf6df5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33737857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1987049a10433f61f985c8a961f2a43c8f01aec18c6d80152fa3fbc3c38a2bf2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1759104000'
# Fri, 29 Aug 2025 17:20:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
VOLUME [/spiped]
# Fri, 29 Aug 2025 17:20:00 GMT
WORKDIR /spiped
# Fri, 29 Aug 2025 17:20:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 17:20:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d2a243ecf382412941b4d6772dba911a8093cf3703c933872fbb7ecc21e27e20`  
		Last Modified: Mon, 29 Sep 2025 23:34:24 GMT  
		Size: 27.9 MB (27946145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e9eedd2de38e34f9c3259b80e737fa7ffbfb18c38b1f08d50dbb49345eb0d7`  
		Last Modified: Tue, 30 Sep 2025 01:01:05 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616c241ba477fd0194fc32c7ae4f77367d65f7cc4dc492ba06ee414e5e2e1769`  
		Last Modified: Tue, 30 Sep 2025 01:01:05 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62532e7e306eaf6c857c1dcac69b720b1f9d66d14712934fe28bf0a4be73f567`  
		Last Modified: Tue, 30 Sep 2025 01:01:05 GMT  
		Size: 5.8 MB (5789345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfaf6902331c4ccad828cfb4d679d658a030950d2c261496bd7e99ee3522ce2`  
		Last Modified: Tue, 30 Sep 2025 01:01:05 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3fe9a7ee86cc167f3246c7ccbaca7e78f1107bcb72fdff9d7524c789bdafd50`  
		Last Modified: Tue, 30 Sep 2025 01:01:05 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:505d2a98a8941d45aca76abca0104a7e8d398561b1ae7927db969818fbfe2537
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:444672c549748ba8acd59e1603ca69ca9739f52248e1194cd651561d40623efa`

```dockerfile
```

-	Layers:
	-	`sha256:5fb828ad140b7db9b7197a184f66219daa0cac03e3e22a9ec8a4419674b5f497`  
		Last Modified: Tue, 30 Sep 2025 07:04:22 GMT  
		Size: 3.6 MB (3619072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fadb488ef6180819b4864740433eb5e2bd6a3c663387cd05aea5ae85c0d45596`  
		Last Modified: Tue, 30 Sep 2025 07:04:23 GMT  
		Size: 15.1 KB (15131 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v7

```console
$ docker pull spiped@sha256:55c1924462ce41de687f42e2603b9295efb3af2ea9416e2c25e3f9fdd34afb64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31794747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b264184152b054bd80ca19a24fec1f4060c0f6c53fd9419139ce0187034c9cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
# Fri, 29 Aug 2025 17:20:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
VOLUME [/spiped]
# Fri, 29 Aug 2025 17:20:00 GMT
WORKDIR /spiped
# Fri, 29 Aug 2025 17:20:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 17:20:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1135c42cd92801939fa6513bb162537bb967d875405841f452ae92aa019e5bfe`  
		Last Modified: Mon, 08 Sep 2025 22:16:32 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df69bf0846187df4227a06f55de71273baee4d386ccb1f98bb6e74ad188874a`  
		Last Modified: Mon, 08 Sep 2025 22:16:38 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1eed6b9285bafc18f4c963dbf92dff69f211d78afcc6e9f6e750147a8681f6`  
		Last Modified: Mon, 08 Sep 2025 22:49:33 GMT  
		Size: 5.6 MB (5584533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a57a1b1c83bb1f19dbbd26fe2bceb4f92d9d7951f1f17fb60d28ca37cfbf8f`  
		Last Modified: Mon, 08 Sep 2025 22:16:41 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3755b9c4ec1e1535de44613e7ff33ce001f5799640318ceaf4187cd1dd428a0f`  
		Last Modified: Mon, 08 Sep 2025 22:16:44 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:b96e349fb89eafa7400bb0137272e43e7aa3f42efcd87d166a136ad9b0e1e783
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef3ecc4e0843e63369fdd1aea3d2a5e46f2f8f891f2a9660bd7b841c5078b335`

```dockerfile
```

-	Layers:
	-	`sha256:416818cdf08bf484514867f324a9c87f81b1fd4a826f731bd0b95c88d8c643d3`  
		Last Modified: Tue, 09 Sep 2025 01:04:25 GMT  
		Size: 3.6 MB (3618193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbc0b5538d2093419837cea2916b8e4b7473900ca2c1c5fcde6d183855056eaf`  
		Last Modified: Tue, 09 Sep 2025 01:04:26 GMT  
		Size: 15.1 KB (15131 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:b30af9feecd6d2d3e060442d3a65f6e96ddfa1a80fed606c84c1f016a2e3ec98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36370794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cd3ed48417c32b96cea00093023ea9133743c7d939098b1666f4dd6e5b6a44b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Fri, 29 Aug 2025 17:20:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
VOLUME [/spiped]
# Fri, 29 Aug 2025 17:20:00 GMT
WORKDIR /spiped
# Fri, 29 Aug 2025 17:20:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 17:20:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf96c895c9ecb8c50b531abc85aae3b4e1618dd151bee2548e8f0f324a66d264`  
		Last Modified: Mon, 08 Sep 2025 22:08:07 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d894fd8e76b8c24189989a2c4edcede7b07f861c7878d352bdfead93f052b114`  
		Last Modified: Mon, 08 Sep 2025 22:08:11 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009c3a2ddeae00427400405aae3478f6145688b476d8e0a6332ec10033d0214a`  
		Last Modified: Mon, 08 Sep 2025 22:31:44 GMT  
		Size: 6.2 MB (6231800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771b828e58dae600ab30ba08fd29c1f6999e6ad1e0046d8130cc9fb4dfa3230b`  
		Last Modified: Mon, 08 Sep 2025 22:08:16 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c538a87d62b081105d070718eebcabf29d31a37763736eaf01e7e57bd1aa4e2f`  
		Last Modified: Mon, 08 Sep 2025 22:08:19 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:b4b6c21230283163829ba358f0011d55d69c385a2cba19fa01e97ee624229b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec6ae267ebdb45e6c8daf2e30f3457f918cd0da29621862f41bb5f294d7e3142`

```dockerfile
```

-	Layers:
	-	`sha256:d5b5755081e9d83cc165f6f2f16af8973276b35a16325e5d6324b4fd57784cce`  
		Last Modified: Mon, 08 Sep 2025 22:04:50 GMT  
		Size: 3.6 MB (3621114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:002e4f513e5bbf2214b3303f88fd4499f1622400a327fbe0721cf244a7d239ed`  
		Last Modified: Mon, 08 Sep 2025 22:04:51 GMT  
		Size: 15.2 KB (15159 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; 386

```console
$ docker pull spiped@sha256:82171e0666e35ff746fbb4f2dfa2952132328bb53429717390797dbe93bfc17e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37734562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f616dd7bbc1f42449fdc926a447f0d4328e9e133a475731c7460bb30db8c2b70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
# Fri, 29 Aug 2025 17:20:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
VOLUME [/spiped]
# Fri, 29 Aug 2025 17:20:00 GMT
WORKDIR /spiped
# Fri, 29 Aug 2025 17:20:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 17:20:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d6e01c57fc6d674eef68e6bfe57a080b0a70c1c25810b7d6e769151bad3645bf`  
		Last Modified: Mon, 08 Sep 2025 21:12:32 GMT  
		Size: 31.3 MB (31289784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fbcdd1371662f71ddb2b23df80fbf351b005debab82aafc902262981ba08ab`  
		Last Modified: Mon, 08 Sep 2025 21:57:17 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85701ac5b161301c0a05e4843ffa9727392f95db70819ce77c42c30226553c80`  
		Last Modified: Mon, 08 Sep 2025 21:57:19 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50bb5031c8241b37a2e696ec8db5c03b82b1bd1ee65904857cfe42b14fac04af`  
		Last Modified: Mon, 08 Sep 2025 21:57:22 GMT  
		Size: 6.4 MB (6442413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934469e6381f737152de5a1b3f6dd1729b3784cf1f1bae109fe5d3529099a832`  
		Last Modified: Mon, 08 Sep 2025 21:57:15 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d17cd8e8171dbc807b1bedab727c5008a91341d002e8f731f019a7f1ed51f3d`  
		Last Modified: Mon, 08 Sep 2025 21:57:14 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:dfafee5c17a53e878812bb4dff43ecef3eca0c87e52722ca1d7d2bfb87c6797a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49def9b4fb17d9ed6e5081b5415496b65daf1abe47fecc43f29182d4729ceb85`

```dockerfile
```

-	Layers:
	-	`sha256:55fc616258ae4fd67f353ff39a69793c11ab295b8f55ee9a3b8a23db68bedd00`  
		Last Modified: Mon, 08 Sep 2025 22:04:56 GMT  
		Size: 3.6 MB (3620207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b3162a00f4793a413edfb2b0c0cac933355d8dc353782e0efb33e4bcd6a98f2`  
		Last Modified: Mon, 08 Sep 2025 22:04:57 GMT  
		Size: 15.0 KB (14989 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; ppc64le

```console
$ docker pull spiped@sha256:dd0f2c26fba6d8f7e91efc7236bc5ae26c6c586ebafbf27ba67b05e7405c585a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40436895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7da8485c8492a65bd7db4a06ef4be5e13fa36922e67991803bd5b1597ce5908d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
# Fri, 29 Aug 2025 17:20:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
VOLUME [/spiped]
# Fri, 29 Aug 2025 17:20:00 GMT
WORKDIR /spiped
# Fri, 29 Aug 2025 17:20:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 17:20:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d11c44105444ef722eccd8c92c6b2fce9986e3274ba9b346e044a458c0425852`  
		Last Modified: Mon, 08 Sep 2025 22:03:02 GMT  
		Size: 33.6 MB (33594351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ff6f5b89d4b84c15ed34cf42385122a4619cef97f26b3b00fcf1ce99826e4e`  
		Last Modified: Tue, 09 Sep 2025 02:16:11 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2147f6accb00e92c1eedf8f3e292138aa51f43b774e82dbf3d236cd25c7a6ef5`  
		Last Modified: Tue, 09 Sep 2025 02:16:12 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b36c08f12f5edbb0ebb0705a1fcbf0751d18146517cd3eac584f7a0e0e7db3`  
		Last Modified: Tue, 09 Sep 2025 02:16:10 GMT  
		Size: 6.8 MB (6840177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c16bd3132d22ed6e04816499858f07b1a6caecb5e593723f22e1c664fd2504`  
		Last Modified: Tue, 09 Sep 2025 02:16:13 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbcf4a0a26c7a4eb0cae2a7bc2b099ccdd386daa17a0388ccc953332ef162ba9`  
		Last Modified: Tue, 09 Sep 2025 02:16:11 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:fdddf2e236221e21497abda9439774a7dfa99c89501e1f61344f91f288ac160b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cc8e6b9798028e08951fd7894a1176bc5de4172976f59bbb7d7a99a1fb24470`

```dockerfile
```

-	Layers:
	-	`sha256:cd3e3f7f121b597b3ae88011a5350cf0229bae2285264b9e515b5f46f48a7b9f`  
		Last Modified: Tue, 09 Sep 2025 04:04:37 GMT  
		Size: 3.6 MB (3621815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:561d39bebbd3a77be83f987074591f029589166e840124add7a2af8871dbfa2d`  
		Last Modified: Tue, 09 Sep 2025 04:04:38 GMT  
		Size: 15.1 KB (15073 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; riscv64

```console
$ docker pull spiped@sha256:5905e53a269c6d922a17fef7fdf180d83935887fa9af99d4d2e1017c1bf4e4b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37631952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ee19633a651738b628f2cb5bd0e550e79df43a149943642e1d7a5141d8ffca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
# Fri, 29 Aug 2025 17:20:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
VOLUME [/spiped]
# Fri, 29 Aug 2025 17:20:00 GMT
WORKDIR /spiped
# Fri, 29 Aug 2025 17:20:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 17:20:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:dd4e3fb8766f676c414c0c55be0f5d9f6e6359dc2628caa804016b0f2ba461f2`  
		Last Modified: Tue, 09 Sep 2025 01:07:45 GMT  
		Size: 28.3 MB (28271372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5608d5fca44bef1f4b578d71749c38d463140bf3ab4d903cacedcf25cbfb9ba6`  
		Last Modified: Thu, 11 Sep 2025 01:25:02 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4bc773262a957de28308fa55f96bedcd0aa74b518d88a7624fa2e0b03fcb251`  
		Last Modified: Thu, 11 Sep 2025 01:25:02 GMT  
		Size: 821.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06bb0e8310deeeeb26569b478133d933e7325ba0b5b5e083af0ad0c073f58a0f`  
		Last Modified: Thu, 11 Sep 2025 01:25:03 GMT  
		Size: 9.4 MB (9358216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e448b353aa48be5bdae79823d76610551cc40a64b4fdeecb7d66e069b12a2a32`  
		Last Modified: Thu, 11 Sep 2025 01:25:02 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6987c22a28e1efb9aeaa5db4d0fbdddda967388660118de93a4b59b50a60a629`  
		Last Modified: Thu, 11 Sep 2025 01:25:02 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:eae3abb229eddf26ee162518ee18852aa3313c5423b849e5a99cfb0bc465a61a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b307618389b5fb8b78449eed1fa709b2b593d2a6a4274a9d447e7dbcb7b0dd99`

```dockerfile
```

-	Layers:
	-	`sha256:87a76192d8d8570e6c6ece1dcc22bd9d1b86f6b5e205dad608d48c2b72e8165d`  
		Last Modified: Thu, 11 Sep 2025 04:04:40 GMT  
		Size: 3.6 MB (3613221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0b18544defcdfecf35f0333ecb448641f877ce0f6f06435d6a33cc8cbeb3172`  
		Last Modified: Thu, 11 Sep 2025 04:04:41 GMT  
		Size: 15.1 KB (15073 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; s390x

```console
$ docker pull spiped@sha256:f43d82c5a3d35f6ce2cddbdf9ec0205301960afbde878d2ca5a7861df01aeb4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35956343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d59764c7f98b190c53b1f7bc6dd3b9098f2d767322d48956bd085d7b071c49c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
# Fri, 29 Aug 2025 17:20:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
VOLUME [/spiped]
# Fri, 29 Aug 2025 17:20:00 GMT
WORKDIR /spiped
# Fri, 29 Aug 2025 17:20:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 17:20:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8af003c0cb712f415b555d33f1c4a9cc3fad82782766d388f3426c4d807a5ab2`  
		Last Modified: Mon, 08 Sep 2025 21:53:51 GMT  
		Size: 29.8 MB (29832904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2763f4a4daec888c7d63b0e0ff81db10dadc52fb53a435fa22ae03ee5decf09a`  
		Last Modified: Tue, 09 Sep 2025 00:21:56 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5161d34bcac535a56ad8efb0d748f8b339da9725c091b74f67c1823ec2bb58d9`  
		Last Modified: Tue, 09 Sep 2025 00:21:59 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4a51a796aa3aaf724cc5bbec39ecd4f3b9a5b8244e1af98a933025d02f4ffd`  
		Last Modified: Tue, 09 Sep 2025 01:21:28 GMT  
		Size: 6.1 MB (6121071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8daf184e635c2a7d701efea95606a1b0e8e8a2a745d9a541e956f2b0b71a39`  
		Last Modified: Tue, 09 Sep 2025 00:22:01 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f4edae4a9a40914726f530d046af5b5b1f4e4c4048a15ee60f70e0ab94f709`  
		Last Modified: Tue, 09 Sep 2025 00:22:05 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:def719779c2d7857b30da66a7a9f95579e191353a797ea6592ccef059ba709e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d10bf28afc205e156ee5a6abfde2d897204f3852cd6ba8108423663144fb84a9`

```dockerfile
```

-	Layers:
	-	`sha256:bab5214c083436ce496b531b010d96bf6ce4fc5d41d6254cd2944891972578bb`  
		Last Modified: Tue, 09 Sep 2025 04:04:44 GMT  
		Size: 3.6 MB (3618441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fc2bc9ff9441d9915eae99b2766d2b72f0d4aa3b4904864a6f976f52fceadeb`  
		Last Modified: Tue, 09 Sep 2025 04:04:46 GMT  
		Size: 15.0 KB (15025 bytes)  
		MIME: application/vnd.in-toto+json
