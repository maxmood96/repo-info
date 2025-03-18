<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `spiped`

-	[`spiped:1`](#spiped1)
-	[`spiped:1-alpine`](#spiped1-alpine)
-	[`spiped:1.6`](#spiped16)
-	[`spiped:1.6-alpine`](#spiped16-alpine)
-	[`spiped:1.6.3`](#spiped163)
-	[`spiped:1.6.3-alpine`](#spiped163-alpine)
-	[`spiped:alpine`](#spipedalpine)
-	[`spiped:latest`](#spipedlatest)

## `spiped:1`

```console
$ docker pull spiped@sha256:fc1f33ece364de511a2a44f0539a7716bea1ec0953fa91c42a303a66cd55b77a
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `spiped:1` - linux; amd64

```console
$ docker pull spiped@sha256:c19bf364bfa9b01e7f25e85f3c4182faa24af4712929de98e36e6a0b7edfd4cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37066454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbfb718114afb7be4711e5fb0bd240c9dd0a669ae1b48d93e3426532a35ba4a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9e666ee2080d653e24746cfb863a5ae3e9a9b21760fd38c5b68d6dd7b3c585`  
		Last Modified: Mon, 17 Mar 2025 23:13:32 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed2bd90f46aec7eec2a2c77a4bb8df89a0a3e132b6f270532ace804fc51464f`  
		Last Modified: Mon, 17 Mar 2025 23:13:32 GMT  
		Size: 2.4 MB (2401370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:993eee5dbd6de6d47b0071ac15523a45b6a8afce9d50daa61807c346f47c266d`  
		Last Modified: Mon, 17 Mar 2025 23:13:32 GMT  
		Size: 6.5 MB (6458678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbd4bf8003cf0865eb03cc5f3d90f07d682ef429b2ac0e65b94c6f010d77b47`  
		Last Modified: Mon, 17 Mar 2025 23:13:32 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:993319058db4392c9db4ba00cbfafbbabede0f3d777fde6728dd4eb483b42ea0`  
		Last Modified: Mon, 17 Mar 2025 23:13:33 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:4e76634ef610cfc556713c4be1a31147ab325ba6832e229407f56e6e02388d0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3530884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4872dedbd739de53112c09fc8399226956b43076779518fea2f0ab2b9795410d`

```dockerfile
```

-	Layers:
	-	`sha256:5f30ebd653ca5651357a3623b460af90e8777573dba62f3f6d6f541434841741`  
		Last Modified: Mon, 17 Mar 2025 23:13:32 GMT  
		Size: 3.5 MB (3515844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b84b0482b1865ead9d5b18a7dac5921be9c7708b96d0604ccc0721d114d442a3`  
		Last Modified: Mon, 17 Mar 2025 23:13:32 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm variant v5

```console
$ docker pull spiped@sha256:7fa569baa2e4571917dcfbfeccc8243ff376678076033123e3833b11906156f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32886160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cc3d47e814f4faffd8aadf598cba98077df9c5e04f8ba3eda699ce802846b01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1740355200'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d8a77b84d73cc90f2bbd622ec970d928c4f14e4be51927c88b7c15b7b6772382`  
		Last Modified: Tue, 25 Feb 2025 01:30:58 GMT  
		Size: 25.7 MB (25740630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8e82324f9ed6ef92c3805276fe1ab8fa8bdd8f407015897c22f32e81556448`  
		Last Modified: Tue, 25 Feb 2025 05:15:19 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18c80389cadb88242cd228219aeb9461304257e925f8811fcbbb470bfd81fd0`  
		Last Modified: Tue, 25 Feb 2025 05:15:19 GMT  
		Size: 2.0 MB (1997208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb256a4313e4774f05ba257deb90ef81ede34bcd9b0d362197570f93fbcf8ad9`  
		Last Modified: Tue, 25 Feb 2025 05:15:19 GMT  
		Size: 5.1 MB (5146780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c3479c48b0ffc4461c5733c985e0bc4325898f27e1607eb84694e696f0ea8b`  
		Last Modified: Tue, 25 Feb 2025 05:15:19 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ec20e1f9a518c4b39a8f5c13cdae21c5d3b60596708602f864327841d36a2c`  
		Last Modified: Tue, 25 Feb 2025 05:15:20 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:3f047eca507cd403c6791648f7c48d66b9349872175c945885648e29b26ce926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3501504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58ec476a13815a2e160b782fa4020274a1005169e66f37c71bd644af3012f18e`

```dockerfile
```

-	Layers:
	-	`sha256:73ec23c96dc073e6f666bf47b1205eb39f3ac9ed516c86358767507b06a4cc1f`  
		Last Modified: Tue, 25 Feb 2025 05:15:19 GMT  
		Size: 3.5 MB (3486362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f8715208bb569facd33c761f2a66848a951deb8cd9e5e1d8777c513a99cbc17`  
		Last Modified: Tue, 25 Feb 2025 05:15:19 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm variant v7

```console
$ docker pull spiped@sha256:99b05b73d0fddf2fa852924722f7219b5185938cac147b249ca64681a980e754
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 MB (30664848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6d3b4bd3bab0abe7d81cf37c4c4a6dc75201aaae6e4f9085f40f01b6bf54d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96913db2d7bf2a45c109be6aa196dc22884e8cccc1cc3b2a39f613a1b90d0943`  
		Last Modified: Tue, 25 Feb 2025 07:02:33 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2566e9b1179e5c8fd6832a19e6629a6862e2021b9fe8d593dca6687eaa0eef0f`  
		Last Modified: Tue, 25 Feb 2025 07:02:33 GMT  
		Size: 1.9 MB (1855566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef718bd99e2a7a5d409e423e94cdc1dd0cbde16231d4c9326956ebeb917a30f7`  
		Last Modified: Tue, 25 Feb 2025 07:02:34 GMT  
		Size: 4.9 MB (4888006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:695edf7c1f3066970e1e3fbae552988aa33f3edf00607d0630d75f52d2e3a950`  
		Last Modified: Tue, 25 Feb 2025 07:02:33 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b009750be7193bc571d7670a73753f454748ca939d25b521e360b5d5c169b91`  
		Last Modified: Tue, 25 Feb 2025 07:02:34 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:893aebd041e27850e114022d592b5dada21e4a35fc0fc0dc4dc7b6d2ab38082f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3500995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec20510c844f5ca50a521741419fe9c064c9892854403176caa8c38145aafd4d`

```dockerfile
```

-	Layers:
	-	`sha256:a5f92c4b0879f8bb8005a8f0e129a938fbacb2e0f6f57d6a84bded5d8e2f203a`  
		Last Modified: Tue, 25 Feb 2025 07:02:33 GMT  
		Size: 3.5 MB (3485853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a94619fd89e6e1f45e5167c17cc1ee967ead21b2a6e15b6f48f1724d8d5671ac`  
		Last Modified: Tue, 25 Feb 2025 07:02:33 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:db53a8c274356cc5da81ada07bb47c61deeb780565f3a80bb603f04a305939e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35788124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:798f3cf34b0f1cc65a81a2efa6db7b05e25dbf4b2535aac42ffb89fb5710c962`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67307fdcfcd65a772010b76ebe296081d6a488e144cdcd1c9d0781cc8f6ea3b6`  
		Last Modified: Tue, 25 Feb 2025 05:20:43 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4da10b03c1db04ea42046a0699a6547ea8fa47cce175e19c4af8db06fbdef1`  
		Last Modified: Tue, 25 Feb 2025 05:20:44 GMT  
		Size: 2.2 MB (2247031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d214314c22c6b6ada301a5df4aab4c5742554fa40efe4ca909ee898af9db44`  
		Last Modified: Tue, 25 Feb 2025 05:20:44 GMT  
		Size: 5.5 MB (5491125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfaaafc3dbcec82ce792cdae6d39e35f6417a7e075534a44b672555735909163`  
		Last Modified: Tue, 25 Feb 2025 05:20:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aeb2d44a802d2f56e52ca4c03efd33ef782441e341d59963b50cc7942cb2665`  
		Last Modified: Tue, 25 Feb 2025 05:20:45 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:1aecc6411bc714ed9b10aa0749e161fc320f2db0704eebb6d7a7517b37e10e9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3502234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a40cdb974e39defc6d4761b60a63bbcea7e9df48f328d4e44582a872027e5bbc`

```dockerfile
```

-	Layers:
	-	`sha256:9bf2b1992699b289df18732bc29ebf544c16efa4f5060b1c01fe821c546fecb2`  
		Last Modified: Tue, 25 Feb 2025 05:20:44 GMT  
		Size: 3.5 MB (3487060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0003b97ac68aada1c31926eb0388cf5715e3c1e094b441d7bd4c2b82fbc6f43f`  
		Last Modified: Tue, 25 Feb 2025 05:20:43 GMT  
		Size: 15.2 KB (15174 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; 386

```console
$ docker pull spiped@sha256:8c3d5a5c56abaaae7abf82cf38241e9b7c8f004a26ccda6ba2257441f3bda2f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37546405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8fd46d4842028eedc1776850f7dd150baf9836168006deed35db9cbbc2e1be9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839e731aef1461390a040cebeeac983c7d9bb1cf3a1b92df974e5d38ab6a5a09`  
		Last Modified: Mon, 17 Mar 2025 23:32:55 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c778ac50739d7d7b86008e98fd5f789cb2cb3987389237d4e6b51d38bf17f9a`  
		Last Modified: Mon, 17 Mar 2025 23:32:55 GMT  
		Size: 2.4 MB (2398675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6d38a505eac9eac7a34554d9c99811feff3b705f79cd6d662e56bba0822a01`  
		Last Modified: Mon, 17 Mar 2025 23:32:55 GMT  
		Size: 6.0 MB (5956664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1ee1056d4f06ee344237cf71c7c1469bb31a29a9478dfa3b259dcc62aaf042`  
		Last Modified: Mon, 17 Mar 2025 23:32:55 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d87efdd8714801b774cf86b2261e9e30d73720eaab82e08cf72d42728094ce`  
		Last Modified: Mon, 17 Mar 2025 23:32:55 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:e35f402ec773de33f2d781228239089173b113441dbe92a071096d943f07e015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bf69b249922ed757f9478e3e2be76cbc4d31b306002dfb5e0df0c6bff530832`

```dockerfile
```

-	Layers:
	-	`sha256:e5a700cd41e3b54827acfc8a7168de1917ba898044ee19a4e6d69de32f5453e6`  
		Last Modified: Mon, 17 Mar 2025 23:32:55 GMT  
		Size: 3.5 MB (3509771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd2af87232f9a80fac7c822128970a4346e9c20ba22b5a1fa0c4c745e534aee2`  
		Last Modified: Mon, 17 Mar 2025 23:32:55 GMT  
		Size: 15.0 KB (15004 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; mips64le

```console
$ docker pull spiped@sha256:f588c7961b2391e29412043bb650c5373ef0d58747e046c824e4aa600b0a3f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36149433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59dcb4aa75e3de41c2a2a75f202d0461f011431c4e2e006675a7821dfd2e2289`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1740355200'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:1851efe37d59b19d5c7092778464657e31dbfae35874c19fb94fb95542e2fba7`  
		Last Modified: Tue, 25 Feb 2025 01:30:49 GMT  
		Size: 28.5 MB (28493681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d443002accadcbf61d00cd6a4ff2148154506b88bafd1824e60d166574549d8a`  
		Last Modified: Tue, 25 Feb 2025 14:46:42 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6876c742899903aae4cab3858c4f7748abc5cdd72cd13499bfd7a31051a866d`  
		Last Modified: Tue, 25 Feb 2025 14:46:43 GMT  
		Size: 1.8 MB (1841111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27741d3453c8dd83a2792eb7f7855412b2783f3aefd7364c79ed196963f092a5`  
		Last Modified: Tue, 25 Feb 2025 14:46:43 GMT  
		Size: 5.8 MB (5813094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9571b92a553f23ec240639ff8c664c5fe98f9ccfb0ad4d9a0e2c11ff8659f682`  
		Last Modified: Tue, 25 Feb 2025 14:46:42 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd4e0b5385ab0445f22fdaaa772ea7005b535d4a354c0ee3852c650fa312b1a`  
		Last Modified: Tue, 25 Feb 2025 14:46:43 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:012cb3dac4ad50d2b5c46601ed61f62a31238587e2632167c3a5b6f339bdc6ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eb9ace30b83120dd844131c6d0936723af680f21c0d081e5e8d98ec0dab8afc`

```dockerfile
```

-	Layers:
	-	`sha256:39a263ac3a5b1feee0dbfba1c9827d227e5a7df25a84e4393b5b59951314b086`  
		Last Modified: Tue, 25 Feb 2025 14:46:42 GMT  
		Size: 14.9 KB (14897 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; ppc64le

```console
$ docker pull spiped@sha256:2d56269c6465cc901bc554cfdb03676cc554945c82b352d308107f5a5bbb8e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41076744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5dd5e4a7a596f710398a998f1c2f30ecf1215b4c0cc62406e61e00c148d721f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff7dfc5ec19a2023a35f359183c5f47a6cc2262506bdfa96caadaea3436edfc`  
		Last Modified: Tue, 25 Feb 2025 04:17:33 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd1c1349f74886a6045e95ddb2858cd4bc0c52f426e9ea28503f764a99b7435`  
		Last Modified: Tue, 25 Feb 2025 04:17:33 GMT  
		Size: 2.6 MB (2582101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c259b563b886cf3310babb5e8c89e8f4d2ba6c99db9282d58b4959d07be769`  
		Last Modified: Tue, 25 Feb 2025 04:17:33 GMT  
		Size: 6.4 MB (6440788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be98953031df8386412e13d3ba09a2448f2f4d9cc5a4be9be1d6767749767fd`  
		Last Modified: Tue, 25 Feb 2025 04:17:33 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336fe8e170289066f18894050bac32156f5d8addae22832618a348398f626ad6`  
		Last Modified: Tue, 25 Feb 2025 04:17:34 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:3c893d4c21851d0dead8263c087e5f1ac53a0397dc3b928b37e088a93f846687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3516589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c075768c2027385e1bc38708b3b1fd535362325c6d869c81800c1f7da1922e64`

```dockerfile
```

-	Layers:
	-	`sha256:8219b097b6744e8b7f9da40627c847256d7a19becc5880ae438b74855641b489`  
		Last Modified: Tue, 25 Feb 2025 04:17:33 GMT  
		Size: 3.5 MB (3501501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8ddb3cb5465f4081c0f39d526cc6e312f4a46ef9614ccaf09c85e70f8c574ee`  
		Last Modified: Tue, 25 Feb 2025 04:17:33 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; s390x

```console
$ docker pull spiped@sha256:263a41c61c6e51a81595bf21d29b293dc8ef1dc6db31846a87528016f6f231c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34326809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:731add486ad8c841f4ee0da0bdf079dd4fc9d95b787f675576b8664cf34ceea6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6d4d169c55c2ee02478b6705c4ba9e6795bffbbb872a22adfd95fb2484f2e85c`  
		Last Modified: Tue, 25 Feb 2025 01:30:03 GMT  
		Size: 26.9 MB (26864838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a09f8852f4de85ce593ec49e5bb2cd625906f3d110243cb6a07a435ebff3c3c`  
		Last Modified: Tue, 25 Feb 2025 03:55:09 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d089fdda46bdb7be319ceec736408cce334720e9f43d43f4f6f571796b8c71f0`  
		Last Modified: Tue, 25 Feb 2025 03:55:09 GMT  
		Size: 2.1 MB (2068731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d178c00425fc4a8b273a41abd4d42f17485cebac65dccb7d2d34bc0f2236a3d`  
		Last Modified: Tue, 25 Feb 2025 03:55:09 GMT  
		Size: 5.4 MB (5391698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ae414cbce0fd75ff49297b77b90536f6edfdbbf9f72143191f2e2f029dc792`  
		Last Modified: Tue, 25 Feb 2025 03:55:09 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19fc135aabe22a7b2f284fdb665b918bb0b3ab9e28745e68ebc4f8729a1eb83`  
		Last Modified: Tue, 25 Feb 2025 03:55:09 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:4338e2c984858a2ff1b2e2c98b9845da59713878e3718b28fc7bead1734e3e22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3519058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c9a1890740bd8c0586f0f8c6feeae6678663abeb76e20e623ec8ed7e47e5765`

```dockerfile
```

-	Layers:
	-	`sha256:b95d1ed970c8f6578ef0c5440e8984ce588648a047a69f64ccab2c2251305422`  
		Last Modified: Tue, 25 Feb 2025 03:55:09 GMT  
		Size: 3.5 MB (3504018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6033e6dc86c10bc0920271bace69a7abbf13198adf934992a0f16c0e71d8a2bb`  
		Last Modified: Tue, 25 Feb 2025 03:55:09 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1-alpine`

```console
$ docker pull spiped@sha256:94aba68c45e1ba17bced726cc5ffe072a2b0cbba54eca3b250c1df2ddb8b8a15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
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

### `spiped:1-alpine` - linux; amd64

```console
$ docker pull spiped@sha256:7ac6025838d2bc44ef0e0fafaf5982e0fc4373b688d82fd8fcf05d8b97ca538b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38502c733d8809263c7b9aef9befc5daac0d3a04ff701311a9df754f155a16b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5cbb4d14e8e59f505be1081c094889a892e335b697f6d0c4944a24ea721d7a2`  
		Last Modified: Fri, 14 Feb 2025 19:24:08 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb14bfd2d59e15880cb805303a18fd6fc6bc7e980d9ea46c8fddaf5072a577e7`  
		Last Modified: Fri, 14 Feb 2025 19:24:08 GMT  
		Size: 7.9 KB (7910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f93bc17b0afa3407e99dd41fd4909fb96e359b2cb4612c46ded356003ed053`  
		Last Modified: Fri, 14 Feb 2025 19:24:08 GMT  
		Size: 107.6 KB (107606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d9fa481a10b5130c48f48db6dbbe9a30b114bf719e8fe78001449bca914634`  
		Last Modified: Fri, 14 Feb 2025 19:24:08 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585408ce1d63439f4bd520d967524dbc4d7e05e0d452c10c0dc69c4709d28e50`  
		Last Modified: Fri, 14 Feb 2025 19:24:09 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:91bf4effc5a6d6617632764adb1237e80919976921e5e3964f445b458cdffe5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157e2618e51acb8116b41dc6c3e43f214685385070706f8e531392d2a2b5a32f`

```dockerfile
```

-	Layers:
	-	`sha256:2744be77085e9a3321af7adcd6b3545cf6bfe6ed121b65fb85ada625330919e6`  
		Last Modified: Fri, 14 Feb 2025 19:24:08 GMT  
		Size: 79.8 KB (79822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54db7fc3515a2461325d4de9fc957a390badfaab3a19d15be7868d671af57e54`  
		Last Modified: Fri, 14 Feb 2025 19:24:08 GMT  
		Size: 14.3 KB (14301 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:df12325bd4f67527eef210da2e785cccf9fee709f5839bb817095148b372e4f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3463168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef2998ff82432e374d083b5b629bb256e09097ef1a9f83eea7d0ab00e5516ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066b47e1325b9f6db29d2d135e8ce6b8fcbf90a8f37138d1f3356a294928613b`  
		Last Modified: Fri, 14 Feb 2025 22:09:56 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014f6178dbec0d9fa86b0b438929f32378f60d88338518b7952956c6aa1b5cb7`  
		Last Modified: Fri, 14 Feb 2025 22:09:56 GMT  
		Size: 7.9 KB (7917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6bb96c10a3bddea4cf5fb950ac49b22112a43dc906ac1a150c2651b21621161`  
		Last Modified: Fri, 14 Feb 2025 22:09:56 GMT  
		Size: 89.1 KB (89139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7b5d6ff490ba5ca8f35cbb9b0d65060b194abf98610c588e99805f81d8e35d`  
		Last Modified: Fri, 14 Feb 2025 22:09:56 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ce1526e7b45007e682aa0fd80fbd9c1aa1537c854c4ee7ec3a9ad9037b0b67`  
		Last Modified: Fri, 14 Feb 2025 22:09:57 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:45bcf73666108868c8355e70fce85a00349f2a252225bb8117406a06cb74e674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f115d9a33ace52d319c520b7bfc5952bc13d2e791d27cd9170c8ee19fbeefa12`

```dockerfile
```

-	Layers:
	-	`sha256:787453bd83dce9d473689f5e983cfc99224f335f52dda1d16a0e5b0302d0f106`  
		Last Modified: Fri, 14 Feb 2025 22:09:55 GMT  
		Size: 14.2 KB (14186 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:243dcf0d023243a3b61aee8cb2b205b8fe61fc470d82257934575de8a39dcbc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3189092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4241711a55ea959adb9faab82cba6408126c91cbec6d0af49161185a7031a78a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c19710bb16bad23e16e1942366ab47dc67214cc321581fe20fa6c6ff243be2f`  
		Last Modified: Fri, 14 Feb 2025 21:48:26 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66da5915b0a972b3b239c655a0797a199a02875109463ca9231c3c764542ebec`  
		Last Modified: Fri, 14 Feb 2025 21:48:26 GMT  
		Size: 7.9 KB (7928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e673af941f44b5da1cc7a57b60bb8dc744fb13be7bc3f249e2bffc928309186`  
		Last Modified: Fri, 14 Feb 2025 21:48:26 GMT  
		Size: 81.7 KB (81660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f14c2ace1cb5e92040b8c20569aa9bc1f844aa0a668c66c2e9f43b1d1e71d3`  
		Last Modified: Fri, 14 Feb 2025 21:48:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444ed75a52b489ce3cd4cc2e7a2f1c304b60aca0c041bdbc91901221011420dc`  
		Last Modified: Fri, 14 Feb 2025 21:48:27 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:c53f275713194c826f486ee2d8eaac5d420edc72a311fa688ae6e01b45c058c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90aa7c5afef13f34cc7da917449cd3b867e0efd586073777180b4f3322da556d`

```dockerfile
```

-	Layers:
	-	`sha256:f944c77504e84bfc3b670136a0525be52ff36579d52cf1bdc60500ce40e8cd2b`  
		Last Modified: Fri, 14 Feb 2025 21:48:26 GMT  
		Size: 79.9 KB (79858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:965d6330c884c6fff95b9c9614e372105c03df6e0066d24b9719318d47c7a4fd`  
		Last Modified: Fri, 14 Feb 2025 21:48:26 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:47f6dfb20be478dce9979b1e2494b93143aa488741abf7dc66ba6f515e197d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4102884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f508cb0494d2702e3a13db5d6fc2fd1ca41256c5959e0c4652e04994a249388a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e9ace35db34c3304a810302430fb8aef69b65f583bd5e243d327da73e37c2a`  
		Last Modified: Fri, 14 Feb 2025 22:23:47 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a714b728344222c6dfa8f49bd713be1cc1d83e747cab7f88cfaac3caef9ebe58`  
		Last Modified: Fri, 14 Feb 2025 22:23:47 GMT  
		Size: 7.9 KB (7921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a90c58f039279dd810920bc66f47f0c176890374bc494740bfa97ecbfa53767`  
		Last Modified: Fri, 14 Feb 2025 22:23:48 GMT  
		Size: 100.6 KB (100551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:898ec4dd7aa4832397a2e91d629904b2a48c8298de7db9365c04d33ebbf1bedc`  
		Last Modified: Fri, 14 Feb 2025 22:23:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26adf19273ff38a41503b067a8d1c5a35d4048e2291780e1ffa91def36425f6a`  
		Last Modified: Fri, 14 Feb 2025 22:23:48 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:b00591e00a263982885b0bee54a5d7c27ebcf5249fdaa334c51fc223467aabf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90bf2a0d811c39c7759e43d4257b01711ffdf36fa3dceffc397887cc7f8fa9d0`

```dockerfile
```

-	Layers:
	-	`sha256:c19f26a228bd4be6de3aa9d8196866405d54f8bc38d014c8f26254efe16ae04e`  
		Last Modified: Fri, 14 Feb 2025 22:23:48 GMT  
		Size: 79.9 KB (79878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5a1704deb4400e22af6abe356817cdee187689b0cba34988ce227508adfd78f`  
		Last Modified: Fri, 14 Feb 2025 22:23:48 GMT  
		Size: 14.4 KB (14433 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; 386

```console
$ docker pull spiped@sha256:61b83f6f4da433231db95db1a13fe86dbe85aaecde12dcb9a669f0b0ed0b6e84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3593051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b68ea95baf750c2a2749ec794c8238c510e5792dc8857ed4a3645d071f394823`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89de02b79b34b2bc491f8c7e8607233cc124ed19295cf456e64382e5afc72fbd`  
		Last Modified: Fri, 14 Feb 2025 19:11:58 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff1d235c70003f61e0de885229553d72517e82d7f45df6d561b480b2cd9c5fc`  
		Last Modified: Fri, 14 Feb 2025 19:11:58 GMT  
		Size: 7.9 KB (7914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68a0453a1d3c0248fee96f306a8ede9aa3d7f2dd02652a8dbdff1b0d8c9438b`  
		Last Modified: Fri, 14 Feb 2025 19:11:58 GMT  
		Size: 120.1 KB (120130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e021c9b7ed20e7390deef74c89a7a5540f6309865137308f9a80ac607be260f`  
		Last Modified: Fri, 14 Feb 2025 19:11:58 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2872beb154170ecfc36e7b32d8019cfc1e29a60d26d251929d28131277a7fd0c`  
		Last Modified: Fri, 14 Feb 2025 19:11:59 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:4c3f4670bd80d3c0136a64e6f27ff285948a413faee904ef1c460b8f51d4e516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8c5f2d723a731a066cf77f9a59824e65134fef732e62678056b932016e17282`

```dockerfile
```

-	Layers:
	-	`sha256:b1e174fd16318b9fb1190150ba833822f30825a45606ea9af9ec1723ce03867c`  
		Last Modified: Fri, 14 Feb 2025 19:11:58 GMT  
		Size: 79.8 KB (79797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86e4a7deb35e498340a41c762c8316785005a9ab4e93a2ab0a677fc623e721fd`  
		Last Modified: Fri, 14 Feb 2025 19:11:58 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:0763e833f3d2e767ad7c1ab64d3a1778d9543cffbe2731d7f8c40bee27d44a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3696292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1cde70893ef4a0b94f4624b6bd8ea6a51522d65faf50b2646cac866d386dafe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22ff6ba800883c9495b3d17b7735935035a83bdb153e380d5f5f6c80c3573c5`  
		Last Modified: Fri, 14 Feb 2025 21:51:56 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77eb59aefcf51d96da7771cb0671fa43ebe8e636326ce4db947ff446ea9b4eaa`  
		Last Modified: Fri, 14 Feb 2025 21:51:56 GMT  
		Size: 7.9 KB (7917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b657e1255fd2cfb228ed06e75846652368ff0d80307f8b278c3db5e5558f4f64`  
		Last Modified: Fri, 14 Feb 2025 21:51:56 GMT  
		Size: 112.6 KB (112646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1de73da0d337b9f7fd4e60cf9b67d3592f9e6f6f539421800b167a2735f1bdb`  
		Last Modified: Fri, 14 Feb 2025 21:51:56 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ad280a5133fac353984bead0c9962cf3a9c94714d7806a61832de902c8e929`  
		Last Modified: Fri, 14 Feb 2025 21:51:57 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:522f73a6a1f1e955300602615eb9a993897959108be79c09d235f1db5e488940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 KB (92255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f95185cb2bad6bef09c576b8e4d9d0bf6563783c294a92e69f28b758029f2ac0`

```dockerfile
```

-	Layers:
	-	`sha256:eb306f89b50101c069df46fb92b19620767f2503887c596aedfc415f347a4246`  
		Last Modified: Fri, 14 Feb 2025 21:51:56 GMT  
		Size: 77.9 KB (77905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c821af9afc609e7780dcfb284627dd581cbede4a66c24cc04b41f590c6244531`  
		Last Modified: Fri, 14 Feb 2025 21:51:56 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:4e7de8f9709ec3d17502bc8bb28f682390ca0f28540c21c3a3af3d7c341dc246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3459539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:504149511c6ccc2b6171cb52f835ea33310f60a13cb4f1217042ba7b30d26964`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c30567d05b83d280c92f0fd67f2111b6e24b0ed19d33f47a59b9ff4de364a64`  
		Last Modified: Sun, 16 Feb 2025 05:54:31 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d0963c5b0ae916eb236c2459006edc9e233988196970deb59739005856241f`  
		Last Modified: Sun, 16 Feb 2025 05:54:31 GMT  
		Size: 7.9 KB (7903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92254399fdbccb7d8366a87f97833ee67c515bf8d17be08064a3b25323ec019e`  
		Last Modified: Sun, 16 Feb 2025 05:54:31 GMT  
		Size: 98.8 KB (98811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4b70370fbe28ac9fa59252adef103c1e801b11b4282a7836f323b6f9cfbbf0`  
		Last Modified: Sun, 16 Feb 2025 05:54:31 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421ddf9c5739ee7f0969aac39a6c858cd81ff02ee5f765c215cda1d7404f7ee4`  
		Last Modified: Sun, 16 Feb 2025 05:54:32 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f9cc83e697345dc797170082bb5f58796e3c4247db4a7e9dc9a18c5f5d770c1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9082f8d0a7bf47b624f56e71a3e3aa17d3af84359fece9dc0ba70c14b635f7f5`

```dockerfile
```

-	Layers:
	-	`sha256:e79532d7edd009e631ef81e580e98cd57bd38a27218b471ca6d59658abf18da4`  
		Last Modified: Sun, 16 Feb 2025 05:54:31 GMT  
		Size: 77.9 KB (77901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5a81928e2faccb215eabff958751f6bd93127a2016536154fd6142ca42fad06`  
		Last Modified: Sun, 16 Feb 2025 05:54:31 GMT  
		Size: 14.3 KB (14346 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:de25b12e766fe57e24177257227c53d5a27fc1a3ca4abe48e8bc60e0351bdaef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62cb095475057abb702522c9d705013168c8522d986f39b9047739ee6efe16b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a28161d111a002ad388fefdd709f7bb67cb61071bfdfa7960202816d14c2e2`  
		Last Modified: Fri, 14 Feb 2025 22:26:10 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30984a12769648824acad7e1386b7ba7193bf81929e37f44ce5f3c04f82acc6`  
		Last Modified: Fri, 14 Feb 2025 22:26:10 GMT  
		Size: 7.9 KB (7915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b5b85eee8dde04ba3dbc50eb3b644d79d18255b1eb4dfa5c888403b0ad97cc`  
		Last Modified: Fri, 14 Feb 2025 22:26:10 GMT  
		Size: 96.9 KB (96918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8860fa829f189bb5e960d5036162d15a1aac72e9ce8bed6c40b68549752c2199`  
		Last Modified: Fri, 14 Feb 2025 22:26:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb23aa9487acbddced4252bb38b3510de48d049a3a347fcfb6b24f40c9ff730`  
		Last Modified: Fri, 14 Feb 2025 22:26:11 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:2065dca98493b203898ab91ad7de40fb703351116ab3bfc12c9a52026ce6c13e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f932f07832d03eeec80862781aec2cb3efb7c48fadec873786bd1c8af939e6f5`

```dockerfile
```

-	Layers:
	-	`sha256:8b919ae512d1430c2c7488ea884c9bc49e2ae21b5170043f2a370c90e9af6c60`  
		Last Modified: Fri, 14 Feb 2025 22:26:10 GMT  
		Size: 77.9 KB (77871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddf9c418603cd0c1fdf650dfd352e9ae11c6eec907de4024a31a994019249053`  
		Last Modified: Fri, 14 Feb 2025 22:26:10 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6`

```console
$ docker pull spiped@sha256:fc1f33ece364de511a2a44f0539a7716bea1ec0953fa91c42a303a66cd55b77a
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `spiped:1.6` - linux; amd64

```console
$ docker pull spiped@sha256:c19bf364bfa9b01e7f25e85f3c4182faa24af4712929de98e36e6a0b7edfd4cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37066454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbfb718114afb7be4711e5fb0bd240c9dd0a669ae1b48d93e3426532a35ba4a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9e666ee2080d653e24746cfb863a5ae3e9a9b21760fd38c5b68d6dd7b3c585`  
		Last Modified: Mon, 17 Mar 2025 23:13:32 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed2bd90f46aec7eec2a2c77a4bb8df89a0a3e132b6f270532ace804fc51464f`  
		Last Modified: Mon, 17 Mar 2025 23:13:32 GMT  
		Size: 2.4 MB (2401370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:993eee5dbd6de6d47b0071ac15523a45b6a8afce9d50daa61807c346f47c266d`  
		Last Modified: Mon, 17 Mar 2025 23:13:32 GMT  
		Size: 6.5 MB (6458678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbd4bf8003cf0865eb03cc5f3d90f07d682ef429b2ac0e65b94c6f010d77b47`  
		Last Modified: Mon, 17 Mar 2025 23:13:32 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:993319058db4392c9db4ba00cbfafbbabede0f3d777fde6728dd4eb483b42ea0`  
		Last Modified: Mon, 17 Mar 2025 23:13:33 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:4e76634ef610cfc556713c4be1a31147ab325ba6832e229407f56e6e02388d0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3530884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4872dedbd739de53112c09fc8399226956b43076779518fea2f0ab2b9795410d`

```dockerfile
```

-	Layers:
	-	`sha256:5f30ebd653ca5651357a3623b460af90e8777573dba62f3f6d6f541434841741`  
		Last Modified: Mon, 17 Mar 2025 23:13:32 GMT  
		Size: 3.5 MB (3515844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b84b0482b1865ead9d5b18a7dac5921be9c7708b96d0604ccc0721d114d442a3`  
		Last Modified: Mon, 17 Mar 2025 23:13:32 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm variant v5

```console
$ docker pull spiped@sha256:7fa569baa2e4571917dcfbfeccc8243ff376678076033123e3833b11906156f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32886160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cc3d47e814f4faffd8aadf598cba98077df9c5e04f8ba3eda699ce802846b01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1740355200'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d8a77b84d73cc90f2bbd622ec970d928c4f14e4be51927c88b7c15b7b6772382`  
		Last Modified: Tue, 25 Feb 2025 01:30:58 GMT  
		Size: 25.7 MB (25740630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8e82324f9ed6ef92c3805276fe1ab8fa8bdd8f407015897c22f32e81556448`  
		Last Modified: Tue, 25 Feb 2025 05:15:19 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18c80389cadb88242cd228219aeb9461304257e925f8811fcbbb470bfd81fd0`  
		Last Modified: Tue, 25 Feb 2025 05:15:19 GMT  
		Size: 2.0 MB (1997208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb256a4313e4774f05ba257deb90ef81ede34bcd9b0d362197570f93fbcf8ad9`  
		Last Modified: Tue, 25 Feb 2025 05:15:19 GMT  
		Size: 5.1 MB (5146780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c3479c48b0ffc4461c5733c985e0bc4325898f27e1607eb84694e696f0ea8b`  
		Last Modified: Tue, 25 Feb 2025 05:15:19 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ec20e1f9a518c4b39a8f5c13cdae21c5d3b60596708602f864327841d36a2c`  
		Last Modified: Tue, 25 Feb 2025 05:15:20 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:3f047eca507cd403c6791648f7c48d66b9349872175c945885648e29b26ce926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3501504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58ec476a13815a2e160b782fa4020274a1005169e66f37c71bd644af3012f18e`

```dockerfile
```

-	Layers:
	-	`sha256:73ec23c96dc073e6f666bf47b1205eb39f3ac9ed516c86358767507b06a4cc1f`  
		Last Modified: Tue, 25 Feb 2025 05:15:19 GMT  
		Size: 3.5 MB (3486362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f8715208bb569facd33c761f2a66848a951deb8cd9e5e1d8777c513a99cbc17`  
		Last Modified: Tue, 25 Feb 2025 05:15:19 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm variant v7

```console
$ docker pull spiped@sha256:99b05b73d0fddf2fa852924722f7219b5185938cac147b249ca64681a980e754
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 MB (30664848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6d3b4bd3bab0abe7d81cf37c4c4a6dc75201aaae6e4f9085f40f01b6bf54d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96913db2d7bf2a45c109be6aa196dc22884e8cccc1cc3b2a39f613a1b90d0943`  
		Last Modified: Tue, 25 Feb 2025 07:02:33 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2566e9b1179e5c8fd6832a19e6629a6862e2021b9fe8d593dca6687eaa0eef0f`  
		Last Modified: Tue, 25 Feb 2025 07:02:33 GMT  
		Size: 1.9 MB (1855566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef718bd99e2a7a5d409e423e94cdc1dd0cbde16231d4c9326956ebeb917a30f7`  
		Last Modified: Tue, 25 Feb 2025 07:02:34 GMT  
		Size: 4.9 MB (4888006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:695edf7c1f3066970e1e3fbae552988aa33f3edf00607d0630d75f52d2e3a950`  
		Last Modified: Tue, 25 Feb 2025 07:02:33 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b009750be7193bc571d7670a73753f454748ca939d25b521e360b5d5c169b91`  
		Last Modified: Tue, 25 Feb 2025 07:02:34 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:893aebd041e27850e114022d592b5dada21e4a35fc0fc0dc4dc7b6d2ab38082f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3500995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec20510c844f5ca50a521741419fe9c064c9892854403176caa8c38145aafd4d`

```dockerfile
```

-	Layers:
	-	`sha256:a5f92c4b0879f8bb8005a8f0e129a938fbacb2e0f6f57d6a84bded5d8e2f203a`  
		Last Modified: Tue, 25 Feb 2025 07:02:33 GMT  
		Size: 3.5 MB (3485853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a94619fd89e6e1f45e5167c17cc1ee967ead21b2a6e15b6f48f1724d8d5671ac`  
		Last Modified: Tue, 25 Feb 2025 07:02:33 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:db53a8c274356cc5da81ada07bb47c61deeb780565f3a80bb603f04a305939e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35788124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:798f3cf34b0f1cc65a81a2efa6db7b05e25dbf4b2535aac42ffb89fb5710c962`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67307fdcfcd65a772010b76ebe296081d6a488e144cdcd1c9d0781cc8f6ea3b6`  
		Last Modified: Tue, 25 Feb 2025 05:20:43 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4da10b03c1db04ea42046a0699a6547ea8fa47cce175e19c4af8db06fbdef1`  
		Last Modified: Tue, 25 Feb 2025 05:20:44 GMT  
		Size: 2.2 MB (2247031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d214314c22c6b6ada301a5df4aab4c5742554fa40efe4ca909ee898af9db44`  
		Last Modified: Tue, 25 Feb 2025 05:20:44 GMT  
		Size: 5.5 MB (5491125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfaaafc3dbcec82ce792cdae6d39e35f6417a7e075534a44b672555735909163`  
		Last Modified: Tue, 25 Feb 2025 05:20:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aeb2d44a802d2f56e52ca4c03efd33ef782441e341d59963b50cc7942cb2665`  
		Last Modified: Tue, 25 Feb 2025 05:20:45 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:1aecc6411bc714ed9b10aa0749e161fc320f2db0704eebb6d7a7517b37e10e9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3502234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a40cdb974e39defc6d4761b60a63bbcea7e9df48f328d4e44582a872027e5bbc`

```dockerfile
```

-	Layers:
	-	`sha256:9bf2b1992699b289df18732bc29ebf544c16efa4f5060b1c01fe821c546fecb2`  
		Last Modified: Tue, 25 Feb 2025 05:20:44 GMT  
		Size: 3.5 MB (3487060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0003b97ac68aada1c31926eb0388cf5715e3c1e094b441d7bd4c2b82fbc6f43f`  
		Last Modified: Tue, 25 Feb 2025 05:20:43 GMT  
		Size: 15.2 KB (15174 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; 386

```console
$ docker pull spiped@sha256:8c3d5a5c56abaaae7abf82cf38241e9b7c8f004a26ccda6ba2257441f3bda2f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37546405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8fd46d4842028eedc1776850f7dd150baf9836168006deed35db9cbbc2e1be9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839e731aef1461390a040cebeeac983c7d9bb1cf3a1b92df974e5d38ab6a5a09`  
		Last Modified: Mon, 17 Mar 2025 23:32:55 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c778ac50739d7d7b86008e98fd5f789cb2cb3987389237d4e6b51d38bf17f9a`  
		Last Modified: Mon, 17 Mar 2025 23:32:55 GMT  
		Size: 2.4 MB (2398675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6d38a505eac9eac7a34554d9c99811feff3b705f79cd6d662e56bba0822a01`  
		Last Modified: Mon, 17 Mar 2025 23:32:55 GMT  
		Size: 6.0 MB (5956664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1ee1056d4f06ee344237cf71c7c1469bb31a29a9478dfa3b259dcc62aaf042`  
		Last Modified: Mon, 17 Mar 2025 23:32:55 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d87efdd8714801b774cf86b2261e9e30d73720eaab82e08cf72d42728094ce`  
		Last Modified: Mon, 17 Mar 2025 23:32:55 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:e35f402ec773de33f2d781228239089173b113441dbe92a071096d943f07e015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bf69b249922ed757f9478e3e2be76cbc4d31b306002dfb5e0df0c6bff530832`

```dockerfile
```

-	Layers:
	-	`sha256:e5a700cd41e3b54827acfc8a7168de1917ba898044ee19a4e6d69de32f5453e6`  
		Last Modified: Mon, 17 Mar 2025 23:32:55 GMT  
		Size: 3.5 MB (3509771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd2af87232f9a80fac7c822128970a4346e9c20ba22b5a1fa0c4c745e534aee2`  
		Last Modified: Mon, 17 Mar 2025 23:32:55 GMT  
		Size: 15.0 KB (15004 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; mips64le

```console
$ docker pull spiped@sha256:f588c7961b2391e29412043bb650c5373ef0d58747e046c824e4aa600b0a3f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36149433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59dcb4aa75e3de41c2a2a75f202d0461f011431c4e2e006675a7821dfd2e2289`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1740355200'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:1851efe37d59b19d5c7092778464657e31dbfae35874c19fb94fb95542e2fba7`  
		Last Modified: Tue, 25 Feb 2025 01:30:49 GMT  
		Size: 28.5 MB (28493681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d443002accadcbf61d00cd6a4ff2148154506b88bafd1824e60d166574549d8a`  
		Last Modified: Tue, 25 Feb 2025 14:46:42 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6876c742899903aae4cab3858c4f7748abc5cdd72cd13499bfd7a31051a866d`  
		Last Modified: Tue, 25 Feb 2025 14:46:43 GMT  
		Size: 1.8 MB (1841111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27741d3453c8dd83a2792eb7f7855412b2783f3aefd7364c79ed196963f092a5`  
		Last Modified: Tue, 25 Feb 2025 14:46:43 GMT  
		Size: 5.8 MB (5813094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9571b92a553f23ec240639ff8c664c5fe98f9ccfb0ad4d9a0e2c11ff8659f682`  
		Last Modified: Tue, 25 Feb 2025 14:46:42 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd4e0b5385ab0445f22fdaaa772ea7005b535d4a354c0ee3852c650fa312b1a`  
		Last Modified: Tue, 25 Feb 2025 14:46:43 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:012cb3dac4ad50d2b5c46601ed61f62a31238587e2632167c3a5b6f339bdc6ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eb9ace30b83120dd844131c6d0936723af680f21c0d081e5e8d98ec0dab8afc`

```dockerfile
```

-	Layers:
	-	`sha256:39a263ac3a5b1feee0dbfba1c9827d227e5a7df25a84e4393b5b59951314b086`  
		Last Modified: Tue, 25 Feb 2025 14:46:42 GMT  
		Size: 14.9 KB (14897 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; ppc64le

```console
$ docker pull spiped@sha256:2d56269c6465cc901bc554cfdb03676cc554945c82b352d308107f5a5bbb8e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41076744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5dd5e4a7a596f710398a998f1c2f30ecf1215b4c0cc62406e61e00c148d721f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff7dfc5ec19a2023a35f359183c5f47a6cc2262506bdfa96caadaea3436edfc`  
		Last Modified: Tue, 25 Feb 2025 04:17:33 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd1c1349f74886a6045e95ddb2858cd4bc0c52f426e9ea28503f764a99b7435`  
		Last Modified: Tue, 25 Feb 2025 04:17:33 GMT  
		Size: 2.6 MB (2582101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c259b563b886cf3310babb5e8c89e8f4d2ba6c99db9282d58b4959d07be769`  
		Last Modified: Tue, 25 Feb 2025 04:17:33 GMT  
		Size: 6.4 MB (6440788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be98953031df8386412e13d3ba09a2448f2f4d9cc5a4be9be1d6767749767fd`  
		Last Modified: Tue, 25 Feb 2025 04:17:33 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336fe8e170289066f18894050bac32156f5d8addae22832618a348398f626ad6`  
		Last Modified: Tue, 25 Feb 2025 04:17:34 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:3c893d4c21851d0dead8263c087e5f1ac53a0397dc3b928b37e088a93f846687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3516589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c075768c2027385e1bc38708b3b1fd535362325c6d869c81800c1f7da1922e64`

```dockerfile
```

-	Layers:
	-	`sha256:8219b097b6744e8b7f9da40627c847256d7a19becc5880ae438b74855641b489`  
		Last Modified: Tue, 25 Feb 2025 04:17:33 GMT  
		Size: 3.5 MB (3501501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8ddb3cb5465f4081c0f39d526cc6e312f4a46ef9614ccaf09c85e70f8c574ee`  
		Last Modified: Tue, 25 Feb 2025 04:17:33 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; s390x

```console
$ docker pull spiped@sha256:263a41c61c6e51a81595bf21d29b293dc8ef1dc6db31846a87528016f6f231c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34326809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:731add486ad8c841f4ee0da0bdf079dd4fc9d95b787f675576b8664cf34ceea6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6d4d169c55c2ee02478b6705c4ba9e6795bffbbb872a22adfd95fb2484f2e85c`  
		Last Modified: Tue, 25 Feb 2025 01:30:03 GMT  
		Size: 26.9 MB (26864838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a09f8852f4de85ce593ec49e5bb2cd625906f3d110243cb6a07a435ebff3c3c`  
		Last Modified: Tue, 25 Feb 2025 03:55:09 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d089fdda46bdb7be319ceec736408cce334720e9f43d43f4f6f571796b8c71f0`  
		Last Modified: Tue, 25 Feb 2025 03:55:09 GMT  
		Size: 2.1 MB (2068731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d178c00425fc4a8b273a41abd4d42f17485cebac65dccb7d2d34bc0f2236a3d`  
		Last Modified: Tue, 25 Feb 2025 03:55:09 GMT  
		Size: 5.4 MB (5391698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ae414cbce0fd75ff49297b77b90536f6edfdbbf9f72143191f2e2f029dc792`  
		Last Modified: Tue, 25 Feb 2025 03:55:09 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19fc135aabe22a7b2f284fdb665b918bb0b3ab9e28745e68ebc4f8729a1eb83`  
		Last Modified: Tue, 25 Feb 2025 03:55:09 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:4338e2c984858a2ff1b2e2c98b9845da59713878e3718b28fc7bead1734e3e22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3519058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c9a1890740bd8c0586f0f8c6feeae6678663abeb76e20e623ec8ed7e47e5765`

```dockerfile
```

-	Layers:
	-	`sha256:b95d1ed970c8f6578ef0c5440e8984ce588648a047a69f64ccab2c2251305422`  
		Last Modified: Tue, 25 Feb 2025 03:55:09 GMT  
		Size: 3.5 MB (3504018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6033e6dc86c10bc0920271bace69a7abbf13198adf934992a0f16c0e71d8a2bb`  
		Last Modified: Tue, 25 Feb 2025 03:55:09 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6-alpine`

```console
$ docker pull spiped@sha256:94aba68c45e1ba17bced726cc5ffe072a2b0cbba54eca3b250c1df2ddb8b8a15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
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

### `spiped:1.6-alpine` - linux; amd64

```console
$ docker pull spiped@sha256:7ac6025838d2bc44ef0e0fafaf5982e0fc4373b688d82fd8fcf05d8b97ca538b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38502c733d8809263c7b9aef9befc5daac0d3a04ff701311a9df754f155a16b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5cbb4d14e8e59f505be1081c094889a892e335b697f6d0c4944a24ea721d7a2`  
		Last Modified: Fri, 14 Feb 2025 19:24:08 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb14bfd2d59e15880cb805303a18fd6fc6bc7e980d9ea46c8fddaf5072a577e7`  
		Last Modified: Fri, 14 Feb 2025 19:24:08 GMT  
		Size: 7.9 KB (7910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f93bc17b0afa3407e99dd41fd4909fb96e359b2cb4612c46ded356003ed053`  
		Last Modified: Fri, 14 Feb 2025 19:24:08 GMT  
		Size: 107.6 KB (107606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d9fa481a10b5130c48f48db6dbbe9a30b114bf719e8fe78001449bca914634`  
		Last Modified: Fri, 14 Feb 2025 19:24:08 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585408ce1d63439f4bd520d967524dbc4d7e05e0d452c10c0dc69c4709d28e50`  
		Last Modified: Fri, 14 Feb 2025 19:24:09 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:91bf4effc5a6d6617632764adb1237e80919976921e5e3964f445b458cdffe5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157e2618e51acb8116b41dc6c3e43f214685385070706f8e531392d2a2b5a32f`

```dockerfile
```

-	Layers:
	-	`sha256:2744be77085e9a3321af7adcd6b3545cf6bfe6ed121b65fb85ada625330919e6`  
		Last Modified: Fri, 14 Feb 2025 19:24:08 GMT  
		Size: 79.8 KB (79822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54db7fc3515a2461325d4de9fc957a390badfaab3a19d15be7868d671af57e54`  
		Last Modified: Fri, 14 Feb 2025 19:24:08 GMT  
		Size: 14.3 KB (14301 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:df12325bd4f67527eef210da2e785cccf9fee709f5839bb817095148b372e4f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3463168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef2998ff82432e374d083b5b629bb256e09097ef1a9f83eea7d0ab00e5516ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066b47e1325b9f6db29d2d135e8ce6b8fcbf90a8f37138d1f3356a294928613b`  
		Last Modified: Fri, 14 Feb 2025 22:09:56 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014f6178dbec0d9fa86b0b438929f32378f60d88338518b7952956c6aa1b5cb7`  
		Last Modified: Fri, 14 Feb 2025 22:09:56 GMT  
		Size: 7.9 KB (7917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6bb96c10a3bddea4cf5fb950ac49b22112a43dc906ac1a150c2651b21621161`  
		Last Modified: Fri, 14 Feb 2025 22:09:56 GMT  
		Size: 89.1 KB (89139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7b5d6ff490ba5ca8f35cbb9b0d65060b194abf98610c588e99805f81d8e35d`  
		Last Modified: Fri, 14 Feb 2025 22:09:56 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ce1526e7b45007e682aa0fd80fbd9c1aa1537c854c4ee7ec3a9ad9037b0b67`  
		Last Modified: Fri, 14 Feb 2025 22:09:57 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:45bcf73666108868c8355e70fce85a00349f2a252225bb8117406a06cb74e674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f115d9a33ace52d319c520b7bfc5952bc13d2e791d27cd9170c8ee19fbeefa12`

```dockerfile
```

-	Layers:
	-	`sha256:787453bd83dce9d473689f5e983cfc99224f335f52dda1d16a0e5b0302d0f106`  
		Last Modified: Fri, 14 Feb 2025 22:09:55 GMT  
		Size: 14.2 KB (14186 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:243dcf0d023243a3b61aee8cb2b205b8fe61fc470d82257934575de8a39dcbc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3189092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4241711a55ea959adb9faab82cba6408126c91cbec6d0af49161185a7031a78a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c19710bb16bad23e16e1942366ab47dc67214cc321581fe20fa6c6ff243be2f`  
		Last Modified: Fri, 14 Feb 2025 21:48:26 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66da5915b0a972b3b239c655a0797a199a02875109463ca9231c3c764542ebec`  
		Last Modified: Fri, 14 Feb 2025 21:48:26 GMT  
		Size: 7.9 KB (7928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e673af941f44b5da1cc7a57b60bb8dc744fb13be7bc3f249e2bffc928309186`  
		Last Modified: Fri, 14 Feb 2025 21:48:26 GMT  
		Size: 81.7 KB (81660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f14c2ace1cb5e92040b8c20569aa9bc1f844aa0a668c66c2e9f43b1d1e71d3`  
		Last Modified: Fri, 14 Feb 2025 21:48:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444ed75a52b489ce3cd4cc2e7a2f1c304b60aca0c041bdbc91901221011420dc`  
		Last Modified: Fri, 14 Feb 2025 21:48:27 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:c53f275713194c826f486ee2d8eaac5d420edc72a311fa688ae6e01b45c058c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90aa7c5afef13f34cc7da917449cd3b867e0efd586073777180b4f3322da556d`

```dockerfile
```

-	Layers:
	-	`sha256:f944c77504e84bfc3b670136a0525be52ff36579d52cf1bdc60500ce40e8cd2b`  
		Last Modified: Fri, 14 Feb 2025 21:48:26 GMT  
		Size: 79.9 KB (79858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:965d6330c884c6fff95b9c9614e372105c03df6e0066d24b9719318d47c7a4fd`  
		Last Modified: Fri, 14 Feb 2025 21:48:26 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:47f6dfb20be478dce9979b1e2494b93143aa488741abf7dc66ba6f515e197d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4102884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f508cb0494d2702e3a13db5d6fc2fd1ca41256c5959e0c4652e04994a249388a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e9ace35db34c3304a810302430fb8aef69b65f583bd5e243d327da73e37c2a`  
		Last Modified: Fri, 14 Feb 2025 22:23:47 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a714b728344222c6dfa8f49bd713be1cc1d83e747cab7f88cfaac3caef9ebe58`  
		Last Modified: Fri, 14 Feb 2025 22:23:47 GMT  
		Size: 7.9 KB (7921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a90c58f039279dd810920bc66f47f0c176890374bc494740bfa97ecbfa53767`  
		Last Modified: Fri, 14 Feb 2025 22:23:48 GMT  
		Size: 100.6 KB (100551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:898ec4dd7aa4832397a2e91d629904b2a48c8298de7db9365c04d33ebbf1bedc`  
		Last Modified: Fri, 14 Feb 2025 22:23:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26adf19273ff38a41503b067a8d1c5a35d4048e2291780e1ffa91def36425f6a`  
		Last Modified: Fri, 14 Feb 2025 22:23:48 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:b00591e00a263982885b0bee54a5d7c27ebcf5249fdaa334c51fc223467aabf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90bf2a0d811c39c7759e43d4257b01711ffdf36fa3dceffc397887cc7f8fa9d0`

```dockerfile
```

-	Layers:
	-	`sha256:c19f26a228bd4be6de3aa9d8196866405d54f8bc38d014c8f26254efe16ae04e`  
		Last Modified: Fri, 14 Feb 2025 22:23:48 GMT  
		Size: 79.9 KB (79878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5a1704deb4400e22af6abe356817cdee187689b0cba34988ce227508adfd78f`  
		Last Modified: Fri, 14 Feb 2025 22:23:48 GMT  
		Size: 14.4 KB (14433 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; 386

```console
$ docker pull spiped@sha256:61b83f6f4da433231db95db1a13fe86dbe85aaecde12dcb9a669f0b0ed0b6e84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3593051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b68ea95baf750c2a2749ec794c8238c510e5792dc8857ed4a3645d071f394823`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89de02b79b34b2bc491f8c7e8607233cc124ed19295cf456e64382e5afc72fbd`  
		Last Modified: Fri, 14 Feb 2025 19:11:58 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff1d235c70003f61e0de885229553d72517e82d7f45df6d561b480b2cd9c5fc`  
		Last Modified: Fri, 14 Feb 2025 19:11:58 GMT  
		Size: 7.9 KB (7914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68a0453a1d3c0248fee96f306a8ede9aa3d7f2dd02652a8dbdff1b0d8c9438b`  
		Last Modified: Fri, 14 Feb 2025 19:11:58 GMT  
		Size: 120.1 KB (120130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e021c9b7ed20e7390deef74c89a7a5540f6309865137308f9a80ac607be260f`  
		Last Modified: Fri, 14 Feb 2025 19:11:58 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2872beb154170ecfc36e7b32d8019cfc1e29a60d26d251929d28131277a7fd0c`  
		Last Modified: Fri, 14 Feb 2025 19:11:59 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:4c3f4670bd80d3c0136a64e6f27ff285948a413faee904ef1c460b8f51d4e516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8c5f2d723a731a066cf77f9a59824e65134fef732e62678056b932016e17282`

```dockerfile
```

-	Layers:
	-	`sha256:b1e174fd16318b9fb1190150ba833822f30825a45606ea9af9ec1723ce03867c`  
		Last Modified: Fri, 14 Feb 2025 19:11:58 GMT  
		Size: 79.8 KB (79797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86e4a7deb35e498340a41c762c8316785005a9ab4e93a2ab0a677fc623e721fd`  
		Last Modified: Fri, 14 Feb 2025 19:11:58 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:0763e833f3d2e767ad7c1ab64d3a1778d9543cffbe2731d7f8c40bee27d44a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3696292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1cde70893ef4a0b94f4624b6bd8ea6a51522d65faf50b2646cac866d386dafe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22ff6ba800883c9495b3d17b7735935035a83bdb153e380d5f5f6c80c3573c5`  
		Last Modified: Fri, 14 Feb 2025 21:51:56 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77eb59aefcf51d96da7771cb0671fa43ebe8e636326ce4db947ff446ea9b4eaa`  
		Last Modified: Fri, 14 Feb 2025 21:51:56 GMT  
		Size: 7.9 KB (7917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b657e1255fd2cfb228ed06e75846652368ff0d80307f8b278c3db5e5558f4f64`  
		Last Modified: Fri, 14 Feb 2025 21:51:56 GMT  
		Size: 112.6 KB (112646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1de73da0d337b9f7fd4e60cf9b67d3592f9e6f6f539421800b167a2735f1bdb`  
		Last Modified: Fri, 14 Feb 2025 21:51:56 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ad280a5133fac353984bead0c9962cf3a9c94714d7806a61832de902c8e929`  
		Last Modified: Fri, 14 Feb 2025 21:51:57 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:522f73a6a1f1e955300602615eb9a993897959108be79c09d235f1db5e488940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 KB (92255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f95185cb2bad6bef09c576b8e4d9d0bf6563783c294a92e69f28b758029f2ac0`

```dockerfile
```

-	Layers:
	-	`sha256:eb306f89b50101c069df46fb92b19620767f2503887c596aedfc415f347a4246`  
		Last Modified: Fri, 14 Feb 2025 21:51:56 GMT  
		Size: 77.9 KB (77905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c821af9afc609e7780dcfb284627dd581cbede4a66c24cc04b41f590c6244531`  
		Last Modified: Fri, 14 Feb 2025 21:51:56 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:4e7de8f9709ec3d17502bc8bb28f682390ca0f28540c21c3a3af3d7c341dc246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3459539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:504149511c6ccc2b6171cb52f835ea33310f60a13cb4f1217042ba7b30d26964`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c30567d05b83d280c92f0fd67f2111b6e24b0ed19d33f47a59b9ff4de364a64`  
		Last Modified: Sun, 16 Feb 2025 05:54:31 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d0963c5b0ae916eb236c2459006edc9e233988196970deb59739005856241f`  
		Last Modified: Sun, 16 Feb 2025 05:54:31 GMT  
		Size: 7.9 KB (7903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92254399fdbccb7d8366a87f97833ee67c515bf8d17be08064a3b25323ec019e`  
		Last Modified: Sun, 16 Feb 2025 05:54:31 GMT  
		Size: 98.8 KB (98811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4b70370fbe28ac9fa59252adef103c1e801b11b4282a7836f323b6f9cfbbf0`  
		Last Modified: Sun, 16 Feb 2025 05:54:31 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421ddf9c5739ee7f0969aac39a6c858cd81ff02ee5f765c215cda1d7404f7ee4`  
		Last Modified: Sun, 16 Feb 2025 05:54:32 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f9cc83e697345dc797170082bb5f58796e3c4247db4a7e9dc9a18c5f5d770c1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9082f8d0a7bf47b624f56e71a3e3aa17d3af84359fece9dc0ba70c14b635f7f5`

```dockerfile
```

-	Layers:
	-	`sha256:e79532d7edd009e631ef81e580e98cd57bd38a27218b471ca6d59658abf18da4`  
		Last Modified: Sun, 16 Feb 2025 05:54:31 GMT  
		Size: 77.9 KB (77901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5a81928e2faccb215eabff958751f6bd93127a2016536154fd6142ca42fad06`  
		Last Modified: Sun, 16 Feb 2025 05:54:31 GMT  
		Size: 14.3 KB (14346 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:de25b12e766fe57e24177257227c53d5a27fc1a3ca4abe48e8bc60e0351bdaef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62cb095475057abb702522c9d705013168c8522d986f39b9047739ee6efe16b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a28161d111a002ad388fefdd709f7bb67cb61071bfdfa7960202816d14c2e2`  
		Last Modified: Fri, 14 Feb 2025 22:26:10 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30984a12769648824acad7e1386b7ba7193bf81929e37f44ce5f3c04f82acc6`  
		Last Modified: Fri, 14 Feb 2025 22:26:10 GMT  
		Size: 7.9 KB (7915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b5b85eee8dde04ba3dbc50eb3b644d79d18255b1eb4dfa5c888403b0ad97cc`  
		Last Modified: Fri, 14 Feb 2025 22:26:10 GMT  
		Size: 96.9 KB (96918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8860fa829f189bb5e960d5036162d15a1aac72e9ce8bed6c40b68549752c2199`  
		Last Modified: Fri, 14 Feb 2025 22:26:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb23aa9487acbddced4252bb38b3510de48d049a3a347fcfb6b24f40c9ff730`  
		Last Modified: Fri, 14 Feb 2025 22:26:11 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:2065dca98493b203898ab91ad7de40fb703351116ab3bfc12c9a52026ce6c13e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f932f07832d03eeec80862781aec2cb3efb7c48fadec873786bd1c8af939e6f5`

```dockerfile
```

-	Layers:
	-	`sha256:8b919ae512d1430c2c7488ea884c9bc49e2ae21b5170043f2a370c90e9af6c60`  
		Last Modified: Fri, 14 Feb 2025 22:26:10 GMT  
		Size: 77.9 KB (77871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddf9c418603cd0c1fdf650dfd352e9ae11c6eec907de4024a31a994019249053`  
		Last Modified: Fri, 14 Feb 2025 22:26:10 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6.3`

```console
$ docker pull spiped@sha256:fc1f33ece364de511a2a44f0539a7716bea1ec0953fa91c42a303a66cd55b77a
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `spiped:1.6.3` - linux; amd64

```console
$ docker pull spiped@sha256:c19bf364bfa9b01e7f25e85f3c4182faa24af4712929de98e36e6a0b7edfd4cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37066454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbfb718114afb7be4711e5fb0bd240c9dd0a669ae1b48d93e3426532a35ba4a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9e666ee2080d653e24746cfb863a5ae3e9a9b21760fd38c5b68d6dd7b3c585`  
		Last Modified: Mon, 17 Mar 2025 23:13:32 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed2bd90f46aec7eec2a2c77a4bb8df89a0a3e132b6f270532ace804fc51464f`  
		Last Modified: Mon, 17 Mar 2025 23:13:32 GMT  
		Size: 2.4 MB (2401370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:993eee5dbd6de6d47b0071ac15523a45b6a8afce9d50daa61807c346f47c266d`  
		Last Modified: Mon, 17 Mar 2025 23:13:32 GMT  
		Size: 6.5 MB (6458678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbd4bf8003cf0865eb03cc5f3d90f07d682ef429b2ac0e65b94c6f010d77b47`  
		Last Modified: Mon, 17 Mar 2025 23:13:32 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:993319058db4392c9db4ba00cbfafbbabede0f3d777fde6728dd4eb483b42ea0`  
		Last Modified: Mon, 17 Mar 2025 23:13:33 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3` - unknown; unknown

```console
$ docker pull spiped@sha256:4e76634ef610cfc556713c4be1a31147ab325ba6832e229407f56e6e02388d0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3530884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4872dedbd739de53112c09fc8399226956b43076779518fea2f0ab2b9795410d`

```dockerfile
```

-	Layers:
	-	`sha256:5f30ebd653ca5651357a3623b460af90e8777573dba62f3f6d6f541434841741`  
		Last Modified: Mon, 17 Mar 2025 23:13:32 GMT  
		Size: 3.5 MB (3515844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b84b0482b1865ead9d5b18a7dac5921be9c7708b96d0604ccc0721d114d442a3`  
		Last Modified: Mon, 17 Mar 2025 23:13:32 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.3` - linux; arm variant v5

```console
$ docker pull spiped@sha256:7fa569baa2e4571917dcfbfeccc8243ff376678076033123e3833b11906156f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32886160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cc3d47e814f4faffd8aadf598cba98077df9c5e04f8ba3eda699ce802846b01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1740355200'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d8a77b84d73cc90f2bbd622ec970d928c4f14e4be51927c88b7c15b7b6772382`  
		Last Modified: Tue, 25 Feb 2025 01:30:58 GMT  
		Size: 25.7 MB (25740630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8e82324f9ed6ef92c3805276fe1ab8fa8bdd8f407015897c22f32e81556448`  
		Last Modified: Tue, 25 Feb 2025 05:15:19 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18c80389cadb88242cd228219aeb9461304257e925f8811fcbbb470bfd81fd0`  
		Last Modified: Tue, 25 Feb 2025 05:15:19 GMT  
		Size: 2.0 MB (1997208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb256a4313e4774f05ba257deb90ef81ede34bcd9b0d362197570f93fbcf8ad9`  
		Last Modified: Tue, 25 Feb 2025 05:15:19 GMT  
		Size: 5.1 MB (5146780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c3479c48b0ffc4461c5733c985e0bc4325898f27e1607eb84694e696f0ea8b`  
		Last Modified: Tue, 25 Feb 2025 05:15:19 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ec20e1f9a518c4b39a8f5c13cdae21c5d3b60596708602f864327841d36a2c`  
		Last Modified: Tue, 25 Feb 2025 05:15:20 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3` - unknown; unknown

```console
$ docker pull spiped@sha256:3f047eca507cd403c6791648f7c48d66b9349872175c945885648e29b26ce926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3501504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58ec476a13815a2e160b782fa4020274a1005169e66f37c71bd644af3012f18e`

```dockerfile
```

-	Layers:
	-	`sha256:73ec23c96dc073e6f666bf47b1205eb39f3ac9ed516c86358767507b06a4cc1f`  
		Last Modified: Tue, 25 Feb 2025 05:15:19 GMT  
		Size: 3.5 MB (3486362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f8715208bb569facd33c761f2a66848a951deb8cd9e5e1d8777c513a99cbc17`  
		Last Modified: Tue, 25 Feb 2025 05:15:19 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.3` - linux; arm variant v7

```console
$ docker pull spiped@sha256:99b05b73d0fddf2fa852924722f7219b5185938cac147b249ca64681a980e754
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 MB (30664848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6d3b4bd3bab0abe7d81cf37c4c4a6dc75201aaae6e4f9085f40f01b6bf54d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96913db2d7bf2a45c109be6aa196dc22884e8cccc1cc3b2a39f613a1b90d0943`  
		Last Modified: Tue, 25 Feb 2025 07:02:33 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2566e9b1179e5c8fd6832a19e6629a6862e2021b9fe8d593dca6687eaa0eef0f`  
		Last Modified: Tue, 25 Feb 2025 07:02:33 GMT  
		Size: 1.9 MB (1855566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef718bd99e2a7a5d409e423e94cdc1dd0cbde16231d4c9326956ebeb917a30f7`  
		Last Modified: Tue, 25 Feb 2025 07:02:34 GMT  
		Size: 4.9 MB (4888006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:695edf7c1f3066970e1e3fbae552988aa33f3edf00607d0630d75f52d2e3a950`  
		Last Modified: Tue, 25 Feb 2025 07:02:33 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b009750be7193bc571d7670a73753f454748ca939d25b521e360b5d5c169b91`  
		Last Modified: Tue, 25 Feb 2025 07:02:34 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3` - unknown; unknown

```console
$ docker pull spiped@sha256:893aebd041e27850e114022d592b5dada21e4a35fc0fc0dc4dc7b6d2ab38082f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3500995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec20510c844f5ca50a521741419fe9c064c9892854403176caa8c38145aafd4d`

```dockerfile
```

-	Layers:
	-	`sha256:a5f92c4b0879f8bb8005a8f0e129a938fbacb2e0f6f57d6a84bded5d8e2f203a`  
		Last Modified: Tue, 25 Feb 2025 07:02:33 GMT  
		Size: 3.5 MB (3485853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a94619fd89e6e1f45e5167c17cc1ee967ead21b2a6e15b6f48f1724d8d5671ac`  
		Last Modified: Tue, 25 Feb 2025 07:02:33 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.3` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:db53a8c274356cc5da81ada07bb47c61deeb780565f3a80bb603f04a305939e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35788124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:798f3cf34b0f1cc65a81a2efa6db7b05e25dbf4b2535aac42ffb89fb5710c962`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67307fdcfcd65a772010b76ebe296081d6a488e144cdcd1c9d0781cc8f6ea3b6`  
		Last Modified: Tue, 25 Feb 2025 05:20:43 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4da10b03c1db04ea42046a0699a6547ea8fa47cce175e19c4af8db06fbdef1`  
		Last Modified: Tue, 25 Feb 2025 05:20:44 GMT  
		Size: 2.2 MB (2247031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d214314c22c6b6ada301a5df4aab4c5742554fa40efe4ca909ee898af9db44`  
		Last Modified: Tue, 25 Feb 2025 05:20:44 GMT  
		Size: 5.5 MB (5491125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfaaafc3dbcec82ce792cdae6d39e35f6417a7e075534a44b672555735909163`  
		Last Modified: Tue, 25 Feb 2025 05:20:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aeb2d44a802d2f56e52ca4c03efd33ef782441e341d59963b50cc7942cb2665`  
		Last Modified: Tue, 25 Feb 2025 05:20:45 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3` - unknown; unknown

```console
$ docker pull spiped@sha256:1aecc6411bc714ed9b10aa0749e161fc320f2db0704eebb6d7a7517b37e10e9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3502234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a40cdb974e39defc6d4761b60a63bbcea7e9df48f328d4e44582a872027e5bbc`

```dockerfile
```

-	Layers:
	-	`sha256:9bf2b1992699b289df18732bc29ebf544c16efa4f5060b1c01fe821c546fecb2`  
		Last Modified: Tue, 25 Feb 2025 05:20:44 GMT  
		Size: 3.5 MB (3487060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0003b97ac68aada1c31926eb0388cf5715e3c1e094b441d7bd4c2b82fbc6f43f`  
		Last Modified: Tue, 25 Feb 2025 05:20:43 GMT  
		Size: 15.2 KB (15174 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.3` - linux; 386

```console
$ docker pull spiped@sha256:8c3d5a5c56abaaae7abf82cf38241e9b7c8f004a26ccda6ba2257441f3bda2f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37546405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8fd46d4842028eedc1776850f7dd150baf9836168006deed35db9cbbc2e1be9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839e731aef1461390a040cebeeac983c7d9bb1cf3a1b92df974e5d38ab6a5a09`  
		Last Modified: Mon, 17 Mar 2025 23:32:55 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c778ac50739d7d7b86008e98fd5f789cb2cb3987389237d4e6b51d38bf17f9a`  
		Last Modified: Mon, 17 Mar 2025 23:32:55 GMT  
		Size: 2.4 MB (2398675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6d38a505eac9eac7a34554d9c99811feff3b705f79cd6d662e56bba0822a01`  
		Last Modified: Mon, 17 Mar 2025 23:32:55 GMT  
		Size: 6.0 MB (5956664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1ee1056d4f06ee344237cf71c7c1469bb31a29a9478dfa3b259dcc62aaf042`  
		Last Modified: Mon, 17 Mar 2025 23:32:55 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d87efdd8714801b774cf86b2261e9e30d73720eaab82e08cf72d42728094ce`  
		Last Modified: Mon, 17 Mar 2025 23:32:55 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3` - unknown; unknown

```console
$ docker pull spiped@sha256:e35f402ec773de33f2d781228239089173b113441dbe92a071096d943f07e015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bf69b249922ed757f9478e3e2be76cbc4d31b306002dfb5e0df0c6bff530832`

```dockerfile
```

-	Layers:
	-	`sha256:e5a700cd41e3b54827acfc8a7168de1917ba898044ee19a4e6d69de32f5453e6`  
		Last Modified: Mon, 17 Mar 2025 23:32:55 GMT  
		Size: 3.5 MB (3509771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd2af87232f9a80fac7c822128970a4346e9c20ba22b5a1fa0c4c745e534aee2`  
		Last Modified: Mon, 17 Mar 2025 23:32:55 GMT  
		Size: 15.0 KB (15004 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.3` - linux; mips64le

```console
$ docker pull spiped@sha256:f588c7961b2391e29412043bb650c5373ef0d58747e046c824e4aa600b0a3f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36149433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59dcb4aa75e3de41c2a2a75f202d0461f011431c4e2e006675a7821dfd2e2289`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1740355200'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:1851efe37d59b19d5c7092778464657e31dbfae35874c19fb94fb95542e2fba7`  
		Last Modified: Tue, 25 Feb 2025 01:30:49 GMT  
		Size: 28.5 MB (28493681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d443002accadcbf61d00cd6a4ff2148154506b88bafd1824e60d166574549d8a`  
		Last Modified: Tue, 25 Feb 2025 14:46:42 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6876c742899903aae4cab3858c4f7748abc5cdd72cd13499bfd7a31051a866d`  
		Last Modified: Tue, 25 Feb 2025 14:46:43 GMT  
		Size: 1.8 MB (1841111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27741d3453c8dd83a2792eb7f7855412b2783f3aefd7364c79ed196963f092a5`  
		Last Modified: Tue, 25 Feb 2025 14:46:43 GMT  
		Size: 5.8 MB (5813094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9571b92a553f23ec240639ff8c664c5fe98f9ccfb0ad4d9a0e2c11ff8659f682`  
		Last Modified: Tue, 25 Feb 2025 14:46:42 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd4e0b5385ab0445f22fdaaa772ea7005b535d4a354c0ee3852c650fa312b1a`  
		Last Modified: Tue, 25 Feb 2025 14:46:43 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3` - unknown; unknown

```console
$ docker pull spiped@sha256:012cb3dac4ad50d2b5c46601ed61f62a31238587e2632167c3a5b6f339bdc6ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eb9ace30b83120dd844131c6d0936723af680f21c0d081e5e8d98ec0dab8afc`

```dockerfile
```

-	Layers:
	-	`sha256:39a263ac3a5b1feee0dbfba1c9827d227e5a7df25a84e4393b5b59951314b086`  
		Last Modified: Tue, 25 Feb 2025 14:46:42 GMT  
		Size: 14.9 KB (14897 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.3` - linux; ppc64le

```console
$ docker pull spiped@sha256:2d56269c6465cc901bc554cfdb03676cc554945c82b352d308107f5a5bbb8e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41076744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5dd5e4a7a596f710398a998f1c2f30ecf1215b4c0cc62406e61e00c148d721f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff7dfc5ec19a2023a35f359183c5f47a6cc2262506bdfa96caadaea3436edfc`  
		Last Modified: Tue, 25 Feb 2025 04:17:33 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd1c1349f74886a6045e95ddb2858cd4bc0c52f426e9ea28503f764a99b7435`  
		Last Modified: Tue, 25 Feb 2025 04:17:33 GMT  
		Size: 2.6 MB (2582101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c259b563b886cf3310babb5e8c89e8f4d2ba6c99db9282d58b4959d07be769`  
		Last Modified: Tue, 25 Feb 2025 04:17:33 GMT  
		Size: 6.4 MB (6440788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be98953031df8386412e13d3ba09a2448f2f4d9cc5a4be9be1d6767749767fd`  
		Last Modified: Tue, 25 Feb 2025 04:17:33 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336fe8e170289066f18894050bac32156f5d8addae22832618a348398f626ad6`  
		Last Modified: Tue, 25 Feb 2025 04:17:34 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3` - unknown; unknown

```console
$ docker pull spiped@sha256:3c893d4c21851d0dead8263c087e5f1ac53a0397dc3b928b37e088a93f846687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3516589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c075768c2027385e1bc38708b3b1fd535362325c6d869c81800c1f7da1922e64`

```dockerfile
```

-	Layers:
	-	`sha256:8219b097b6744e8b7f9da40627c847256d7a19becc5880ae438b74855641b489`  
		Last Modified: Tue, 25 Feb 2025 04:17:33 GMT  
		Size: 3.5 MB (3501501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8ddb3cb5465f4081c0f39d526cc6e312f4a46ef9614ccaf09c85e70f8c574ee`  
		Last Modified: Tue, 25 Feb 2025 04:17:33 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.3` - linux; s390x

```console
$ docker pull spiped@sha256:263a41c61c6e51a81595bf21d29b293dc8ef1dc6db31846a87528016f6f231c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34326809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:731add486ad8c841f4ee0da0bdf079dd4fc9d95b787f675576b8664cf34ceea6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6d4d169c55c2ee02478b6705c4ba9e6795bffbbb872a22adfd95fb2484f2e85c`  
		Last Modified: Tue, 25 Feb 2025 01:30:03 GMT  
		Size: 26.9 MB (26864838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a09f8852f4de85ce593ec49e5bb2cd625906f3d110243cb6a07a435ebff3c3c`  
		Last Modified: Tue, 25 Feb 2025 03:55:09 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d089fdda46bdb7be319ceec736408cce334720e9f43d43f4f6f571796b8c71f0`  
		Last Modified: Tue, 25 Feb 2025 03:55:09 GMT  
		Size: 2.1 MB (2068731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d178c00425fc4a8b273a41abd4d42f17485cebac65dccb7d2d34bc0f2236a3d`  
		Last Modified: Tue, 25 Feb 2025 03:55:09 GMT  
		Size: 5.4 MB (5391698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ae414cbce0fd75ff49297b77b90536f6edfdbbf9f72143191f2e2f029dc792`  
		Last Modified: Tue, 25 Feb 2025 03:55:09 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19fc135aabe22a7b2f284fdb665b918bb0b3ab9e28745e68ebc4f8729a1eb83`  
		Last Modified: Tue, 25 Feb 2025 03:55:09 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3` - unknown; unknown

```console
$ docker pull spiped@sha256:4338e2c984858a2ff1b2e2c98b9845da59713878e3718b28fc7bead1734e3e22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3519058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c9a1890740bd8c0586f0f8c6feeae6678663abeb76e20e623ec8ed7e47e5765`

```dockerfile
```

-	Layers:
	-	`sha256:b95d1ed970c8f6578ef0c5440e8984ce588648a047a69f64ccab2c2251305422`  
		Last Modified: Tue, 25 Feb 2025 03:55:09 GMT  
		Size: 3.5 MB (3504018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6033e6dc86c10bc0920271bace69a7abbf13198adf934992a0f16c0e71d8a2bb`  
		Last Modified: Tue, 25 Feb 2025 03:55:09 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6.3-alpine`

```console
$ docker pull spiped@sha256:94aba68c45e1ba17bced726cc5ffe072a2b0cbba54eca3b250c1df2ddb8b8a15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
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

### `spiped:1.6.3-alpine` - linux; amd64

```console
$ docker pull spiped@sha256:7ac6025838d2bc44ef0e0fafaf5982e0fc4373b688d82fd8fcf05d8b97ca538b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38502c733d8809263c7b9aef9befc5daac0d3a04ff701311a9df754f155a16b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5cbb4d14e8e59f505be1081c094889a892e335b697f6d0c4944a24ea721d7a2`  
		Last Modified: Fri, 14 Feb 2025 19:24:08 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb14bfd2d59e15880cb805303a18fd6fc6bc7e980d9ea46c8fddaf5072a577e7`  
		Last Modified: Fri, 14 Feb 2025 19:24:08 GMT  
		Size: 7.9 KB (7910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f93bc17b0afa3407e99dd41fd4909fb96e359b2cb4612c46ded356003ed053`  
		Last Modified: Fri, 14 Feb 2025 19:24:08 GMT  
		Size: 107.6 KB (107606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d9fa481a10b5130c48f48db6dbbe9a30b114bf719e8fe78001449bca914634`  
		Last Modified: Fri, 14 Feb 2025 19:24:08 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585408ce1d63439f4bd520d967524dbc4d7e05e0d452c10c0dc69c4709d28e50`  
		Last Modified: Fri, 14 Feb 2025 19:24:09 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:91bf4effc5a6d6617632764adb1237e80919976921e5e3964f445b458cdffe5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157e2618e51acb8116b41dc6c3e43f214685385070706f8e531392d2a2b5a32f`

```dockerfile
```

-	Layers:
	-	`sha256:2744be77085e9a3321af7adcd6b3545cf6bfe6ed121b65fb85ada625330919e6`  
		Last Modified: Fri, 14 Feb 2025 19:24:08 GMT  
		Size: 79.8 KB (79822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54db7fc3515a2461325d4de9fc957a390badfaab3a19d15be7868d671af57e54`  
		Last Modified: Fri, 14 Feb 2025 19:24:08 GMT  
		Size: 14.3 KB (14301 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.3-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:df12325bd4f67527eef210da2e785cccf9fee709f5839bb817095148b372e4f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3463168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef2998ff82432e374d083b5b629bb256e09097ef1a9f83eea7d0ab00e5516ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066b47e1325b9f6db29d2d135e8ce6b8fcbf90a8f37138d1f3356a294928613b`  
		Last Modified: Fri, 14 Feb 2025 22:09:56 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014f6178dbec0d9fa86b0b438929f32378f60d88338518b7952956c6aa1b5cb7`  
		Last Modified: Fri, 14 Feb 2025 22:09:56 GMT  
		Size: 7.9 KB (7917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6bb96c10a3bddea4cf5fb950ac49b22112a43dc906ac1a150c2651b21621161`  
		Last Modified: Fri, 14 Feb 2025 22:09:56 GMT  
		Size: 89.1 KB (89139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7b5d6ff490ba5ca8f35cbb9b0d65060b194abf98610c588e99805f81d8e35d`  
		Last Modified: Fri, 14 Feb 2025 22:09:56 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ce1526e7b45007e682aa0fd80fbd9c1aa1537c854c4ee7ec3a9ad9037b0b67`  
		Last Modified: Fri, 14 Feb 2025 22:09:57 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:45bcf73666108868c8355e70fce85a00349f2a252225bb8117406a06cb74e674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f115d9a33ace52d319c520b7bfc5952bc13d2e791d27cd9170c8ee19fbeefa12`

```dockerfile
```

-	Layers:
	-	`sha256:787453bd83dce9d473689f5e983cfc99224f335f52dda1d16a0e5b0302d0f106`  
		Last Modified: Fri, 14 Feb 2025 22:09:55 GMT  
		Size: 14.2 KB (14186 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.3-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:243dcf0d023243a3b61aee8cb2b205b8fe61fc470d82257934575de8a39dcbc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3189092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4241711a55ea959adb9faab82cba6408126c91cbec6d0af49161185a7031a78a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c19710bb16bad23e16e1942366ab47dc67214cc321581fe20fa6c6ff243be2f`  
		Last Modified: Fri, 14 Feb 2025 21:48:26 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66da5915b0a972b3b239c655a0797a199a02875109463ca9231c3c764542ebec`  
		Last Modified: Fri, 14 Feb 2025 21:48:26 GMT  
		Size: 7.9 KB (7928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e673af941f44b5da1cc7a57b60bb8dc744fb13be7bc3f249e2bffc928309186`  
		Last Modified: Fri, 14 Feb 2025 21:48:26 GMT  
		Size: 81.7 KB (81660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f14c2ace1cb5e92040b8c20569aa9bc1f844aa0a668c66c2e9f43b1d1e71d3`  
		Last Modified: Fri, 14 Feb 2025 21:48:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444ed75a52b489ce3cd4cc2e7a2f1c304b60aca0c041bdbc91901221011420dc`  
		Last Modified: Fri, 14 Feb 2025 21:48:27 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:c53f275713194c826f486ee2d8eaac5d420edc72a311fa688ae6e01b45c058c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90aa7c5afef13f34cc7da917449cd3b867e0efd586073777180b4f3322da556d`

```dockerfile
```

-	Layers:
	-	`sha256:f944c77504e84bfc3b670136a0525be52ff36579d52cf1bdc60500ce40e8cd2b`  
		Last Modified: Fri, 14 Feb 2025 21:48:26 GMT  
		Size: 79.9 KB (79858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:965d6330c884c6fff95b9c9614e372105c03df6e0066d24b9719318d47c7a4fd`  
		Last Modified: Fri, 14 Feb 2025 21:48:26 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.3-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:47f6dfb20be478dce9979b1e2494b93143aa488741abf7dc66ba6f515e197d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4102884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f508cb0494d2702e3a13db5d6fc2fd1ca41256c5959e0c4652e04994a249388a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e9ace35db34c3304a810302430fb8aef69b65f583bd5e243d327da73e37c2a`  
		Last Modified: Fri, 14 Feb 2025 22:23:47 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a714b728344222c6dfa8f49bd713be1cc1d83e747cab7f88cfaac3caef9ebe58`  
		Last Modified: Fri, 14 Feb 2025 22:23:47 GMT  
		Size: 7.9 KB (7921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a90c58f039279dd810920bc66f47f0c176890374bc494740bfa97ecbfa53767`  
		Last Modified: Fri, 14 Feb 2025 22:23:48 GMT  
		Size: 100.6 KB (100551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:898ec4dd7aa4832397a2e91d629904b2a48c8298de7db9365c04d33ebbf1bedc`  
		Last Modified: Fri, 14 Feb 2025 22:23:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26adf19273ff38a41503b067a8d1c5a35d4048e2291780e1ffa91def36425f6a`  
		Last Modified: Fri, 14 Feb 2025 22:23:48 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:b00591e00a263982885b0bee54a5d7c27ebcf5249fdaa334c51fc223467aabf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90bf2a0d811c39c7759e43d4257b01711ffdf36fa3dceffc397887cc7f8fa9d0`

```dockerfile
```

-	Layers:
	-	`sha256:c19f26a228bd4be6de3aa9d8196866405d54f8bc38d014c8f26254efe16ae04e`  
		Last Modified: Fri, 14 Feb 2025 22:23:48 GMT  
		Size: 79.9 KB (79878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5a1704deb4400e22af6abe356817cdee187689b0cba34988ce227508adfd78f`  
		Last Modified: Fri, 14 Feb 2025 22:23:48 GMT  
		Size: 14.4 KB (14433 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.3-alpine` - linux; 386

```console
$ docker pull spiped@sha256:61b83f6f4da433231db95db1a13fe86dbe85aaecde12dcb9a669f0b0ed0b6e84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3593051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b68ea95baf750c2a2749ec794c8238c510e5792dc8857ed4a3645d071f394823`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89de02b79b34b2bc491f8c7e8607233cc124ed19295cf456e64382e5afc72fbd`  
		Last Modified: Fri, 14 Feb 2025 19:11:58 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff1d235c70003f61e0de885229553d72517e82d7f45df6d561b480b2cd9c5fc`  
		Last Modified: Fri, 14 Feb 2025 19:11:58 GMT  
		Size: 7.9 KB (7914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68a0453a1d3c0248fee96f306a8ede9aa3d7f2dd02652a8dbdff1b0d8c9438b`  
		Last Modified: Fri, 14 Feb 2025 19:11:58 GMT  
		Size: 120.1 KB (120130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e021c9b7ed20e7390deef74c89a7a5540f6309865137308f9a80ac607be260f`  
		Last Modified: Fri, 14 Feb 2025 19:11:58 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2872beb154170ecfc36e7b32d8019cfc1e29a60d26d251929d28131277a7fd0c`  
		Last Modified: Fri, 14 Feb 2025 19:11:59 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:4c3f4670bd80d3c0136a64e6f27ff285948a413faee904ef1c460b8f51d4e516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8c5f2d723a731a066cf77f9a59824e65134fef732e62678056b932016e17282`

```dockerfile
```

-	Layers:
	-	`sha256:b1e174fd16318b9fb1190150ba833822f30825a45606ea9af9ec1723ce03867c`  
		Last Modified: Fri, 14 Feb 2025 19:11:58 GMT  
		Size: 79.8 KB (79797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86e4a7deb35e498340a41c762c8316785005a9ab4e93a2ab0a677fc623e721fd`  
		Last Modified: Fri, 14 Feb 2025 19:11:58 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.3-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:0763e833f3d2e767ad7c1ab64d3a1778d9543cffbe2731d7f8c40bee27d44a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3696292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1cde70893ef4a0b94f4624b6bd8ea6a51522d65faf50b2646cac866d386dafe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22ff6ba800883c9495b3d17b7735935035a83bdb153e380d5f5f6c80c3573c5`  
		Last Modified: Fri, 14 Feb 2025 21:51:56 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77eb59aefcf51d96da7771cb0671fa43ebe8e636326ce4db947ff446ea9b4eaa`  
		Last Modified: Fri, 14 Feb 2025 21:51:56 GMT  
		Size: 7.9 KB (7917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b657e1255fd2cfb228ed06e75846652368ff0d80307f8b278c3db5e5558f4f64`  
		Last Modified: Fri, 14 Feb 2025 21:51:56 GMT  
		Size: 112.6 KB (112646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1de73da0d337b9f7fd4e60cf9b67d3592f9e6f6f539421800b167a2735f1bdb`  
		Last Modified: Fri, 14 Feb 2025 21:51:56 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ad280a5133fac353984bead0c9962cf3a9c94714d7806a61832de902c8e929`  
		Last Modified: Fri, 14 Feb 2025 21:51:57 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:522f73a6a1f1e955300602615eb9a993897959108be79c09d235f1db5e488940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 KB (92255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f95185cb2bad6bef09c576b8e4d9d0bf6563783c294a92e69f28b758029f2ac0`

```dockerfile
```

-	Layers:
	-	`sha256:eb306f89b50101c069df46fb92b19620767f2503887c596aedfc415f347a4246`  
		Last Modified: Fri, 14 Feb 2025 21:51:56 GMT  
		Size: 77.9 KB (77905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c821af9afc609e7780dcfb284627dd581cbede4a66c24cc04b41f590c6244531`  
		Last Modified: Fri, 14 Feb 2025 21:51:56 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.3-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:4e7de8f9709ec3d17502bc8bb28f682390ca0f28540c21c3a3af3d7c341dc246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3459539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:504149511c6ccc2b6171cb52f835ea33310f60a13cb4f1217042ba7b30d26964`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c30567d05b83d280c92f0fd67f2111b6e24b0ed19d33f47a59b9ff4de364a64`  
		Last Modified: Sun, 16 Feb 2025 05:54:31 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d0963c5b0ae916eb236c2459006edc9e233988196970deb59739005856241f`  
		Last Modified: Sun, 16 Feb 2025 05:54:31 GMT  
		Size: 7.9 KB (7903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92254399fdbccb7d8366a87f97833ee67c515bf8d17be08064a3b25323ec019e`  
		Last Modified: Sun, 16 Feb 2025 05:54:31 GMT  
		Size: 98.8 KB (98811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4b70370fbe28ac9fa59252adef103c1e801b11b4282a7836f323b6f9cfbbf0`  
		Last Modified: Sun, 16 Feb 2025 05:54:31 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421ddf9c5739ee7f0969aac39a6c858cd81ff02ee5f765c215cda1d7404f7ee4`  
		Last Modified: Sun, 16 Feb 2025 05:54:32 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f9cc83e697345dc797170082bb5f58796e3c4247db4a7e9dc9a18c5f5d770c1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9082f8d0a7bf47b624f56e71a3e3aa17d3af84359fece9dc0ba70c14b635f7f5`

```dockerfile
```

-	Layers:
	-	`sha256:e79532d7edd009e631ef81e580e98cd57bd38a27218b471ca6d59658abf18da4`  
		Last Modified: Sun, 16 Feb 2025 05:54:31 GMT  
		Size: 77.9 KB (77901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5a81928e2faccb215eabff958751f6bd93127a2016536154fd6142ca42fad06`  
		Last Modified: Sun, 16 Feb 2025 05:54:31 GMT  
		Size: 14.3 KB (14346 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.3-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:de25b12e766fe57e24177257227c53d5a27fc1a3ca4abe48e8bc60e0351bdaef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62cb095475057abb702522c9d705013168c8522d986f39b9047739ee6efe16b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a28161d111a002ad388fefdd709f7bb67cb61071bfdfa7960202816d14c2e2`  
		Last Modified: Fri, 14 Feb 2025 22:26:10 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30984a12769648824acad7e1386b7ba7193bf81929e37f44ce5f3c04f82acc6`  
		Last Modified: Fri, 14 Feb 2025 22:26:10 GMT  
		Size: 7.9 KB (7915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b5b85eee8dde04ba3dbc50eb3b644d79d18255b1eb4dfa5c888403b0ad97cc`  
		Last Modified: Fri, 14 Feb 2025 22:26:10 GMT  
		Size: 96.9 KB (96918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8860fa829f189bb5e960d5036162d15a1aac72e9ce8bed6c40b68549752c2199`  
		Last Modified: Fri, 14 Feb 2025 22:26:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb23aa9487acbddced4252bb38b3510de48d049a3a347fcfb6b24f40c9ff730`  
		Last Modified: Fri, 14 Feb 2025 22:26:11 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:2065dca98493b203898ab91ad7de40fb703351116ab3bfc12c9a52026ce6c13e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f932f07832d03eeec80862781aec2cb3efb7c48fadec873786bd1c8af939e6f5`

```dockerfile
```

-	Layers:
	-	`sha256:8b919ae512d1430c2c7488ea884c9bc49e2ae21b5170043f2a370c90e9af6c60`  
		Last Modified: Fri, 14 Feb 2025 22:26:10 GMT  
		Size: 77.9 KB (77871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddf9c418603cd0c1fdf650dfd352e9ae11c6eec907de4024a31a994019249053`  
		Last Modified: Fri, 14 Feb 2025 22:26:10 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:alpine`

```console
$ docker pull spiped@sha256:94aba68c45e1ba17bced726cc5ffe072a2b0cbba54eca3b250c1df2ddb8b8a15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
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

### `spiped:alpine` - linux; amd64

```console
$ docker pull spiped@sha256:7ac6025838d2bc44ef0e0fafaf5982e0fc4373b688d82fd8fcf05d8b97ca538b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38502c733d8809263c7b9aef9befc5daac0d3a04ff701311a9df754f155a16b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5cbb4d14e8e59f505be1081c094889a892e335b697f6d0c4944a24ea721d7a2`  
		Last Modified: Fri, 14 Feb 2025 19:24:08 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb14bfd2d59e15880cb805303a18fd6fc6bc7e980d9ea46c8fddaf5072a577e7`  
		Last Modified: Fri, 14 Feb 2025 19:24:08 GMT  
		Size: 7.9 KB (7910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f93bc17b0afa3407e99dd41fd4909fb96e359b2cb4612c46ded356003ed053`  
		Last Modified: Fri, 14 Feb 2025 19:24:08 GMT  
		Size: 107.6 KB (107606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d9fa481a10b5130c48f48db6dbbe9a30b114bf719e8fe78001449bca914634`  
		Last Modified: Fri, 14 Feb 2025 19:24:08 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585408ce1d63439f4bd520d967524dbc4d7e05e0d452c10c0dc69c4709d28e50`  
		Last Modified: Fri, 14 Feb 2025 19:24:09 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:91bf4effc5a6d6617632764adb1237e80919976921e5e3964f445b458cdffe5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157e2618e51acb8116b41dc6c3e43f214685385070706f8e531392d2a2b5a32f`

```dockerfile
```

-	Layers:
	-	`sha256:2744be77085e9a3321af7adcd6b3545cf6bfe6ed121b65fb85ada625330919e6`  
		Last Modified: Fri, 14 Feb 2025 19:24:08 GMT  
		Size: 79.8 KB (79822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54db7fc3515a2461325d4de9fc957a390badfaab3a19d15be7868d671af57e54`  
		Last Modified: Fri, 14 Feb 2025 19:24:08 GMT  
		Size: 14.3 KB (14301 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:df12325bd4f67527eef210da2e785cccf9fee709f5839bb817095148b372e4f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3463168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef2998ff82432e374d083b5b629bb256e09097ef1a9f83eea7d0ab00e5516ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066b47e1325b9f6db29d2d135e8ce6b8fcbf90a8f37138d1f3356a294928613b`  
		Last Modified: Fri, 14 Feb 2025 22:09:56 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014f6178dbec0d9fa86b0b438929f32378f60d88338518b7952956c6aa1b5cb7`  
		Last Modified: Fri, 14 Feb 2025 22:09:56 GMT  
		Size: 7.9 KB (7917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6bb96c10a3bddea4cf5fb950ac49b22112a43dc906ac1a150c2651b21621161`  
		Last Modified: Fri, 14 Feb 2025 22:09:56 GMT  
		Size: 89.1 KB (89139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7b5d6ff490ba5ca8f35cbb9b0d65060b194abf98610c588e99805f81d8e35d`  
		Last Modified: Fri, 14 Feb 2025 22:09:56 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ce1526e7b45007e682aa0fd80fbd9c1aa1537c854c4ee7ec3a9ad9037b0b67`  
		Last Modified: Fri, 14 Feb 2025 22:09:57 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:45bcf73666108868c8355e70fce85a00349f2a252225bb8117406a06cb74e674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f115d9a33ace52d319c520b7bfc5952bc13d2e791d27cd9170c8ee19fbeefa12`

```dockerfile
```

-	Layers:
	-	`sha256:787453bd83dce9d473689f5e983cfc99224f335f52dda1d16a0e5b0302d0f106`  
		Last Modified: Fri, 14 Feb 2025 22:09:55 GMT  
		Size: 14.2 KB (14186 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:243dcf0d023243a3b61aee8cb2b205b8fe61fc470d82257934575de8a39dcbc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3189092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4241711a55ea959adb9faab82cba6408126c91cbec6d0af49161185a7031a78a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c19710bb16bad23e16e1942366ab47dc67214cc321581fe20fa6c6ff243be2f`  
		Last Modified: Fri, 14 Feb 2025 21:48:26 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66da5915b0a972b3b239c655a0797a199a02875109463ca9231c3c764542ebec`  
		Last Modified: Fri, 14 Feb 2025 21:48:26 GMT  
		Size: 7.9 KB (7928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e673af941f44b5da1cc7a57b60bb8dc744fb13be7bc3f249e2bffc928309186`  
		Last Modified: Fri, 14 Feb 2025 21:48:26 GMT  
		Size: 81.7 KB (81660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f14c2ace1cb5e92040b8c20569aa9bc1f844aa0a668c66c2e9f43b1d1e71d3`  
		Last Modified: Fri, 14 Feb 2025 21:48:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444ed75a52b489ce3cd4cc2e7a2f1c304b60aca0c041bdbc91901221011420dc`  
		Last Modified: Fri, 14 Feb 2025 21:48:27 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:c53f275713194c826f486ee2d8eaac5d420edc72a311fa688ae6e01b45c058c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90aa7c5afef13f34cc7da917449cd3b867e0efd586073777180b4f3322da556d`

```dockerfile
```

-	Layers:
	-	`sha256:f944c77504e84bfc3b670136a0525be52ff36579d52cf1bdc60500ce40e8cd2b`  
		Last Modified: Fri, 14 Feb 2025 21:48:26 GMT  
		Size: 79.9 KB (79858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:965d6330c884c6fff95b9c9614e372105c03df6e0066d24b9719318d47c7a4fd`  
		Last Modified: Fri, 14 Feb 2025 21:48:26 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:47f6dfb20be478dce9979b1e2494b93143aa488741abf7dc66ba6f515e197d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4102884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f508cb0494d2702e3a13db5d6fc2fd1ca41256c5959e0c4652e04994a249388a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e9ace35db34c3304a810302430fb8aef69b65f583bd5e243d327da73e37c2a`  
		Last Modified: Fri, 14 Feb 2025 22:23:47 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a714b728344222c6dfa8f49bd713be1cc1d83e747cab7f88cfaac3caef9ebe58`  
		Last Modified: Fri, 14 Feb 2025 22:23:47 GMT  
		Size: 7.9 KB (7921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a90c58f039279dd810920bc66f47f0c176890374bc494740bfa97ecbfa53767`  
		Last Modified: Fri, 14 Feb 2025 22:23:48 GMT  
		Size: 100.6 KB (100551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:898ec4dd7aa4832397a2e91d629904b2a48c8298de7db9365c04d33ebbf1bedc`  
		Last Modified: Fri, 14 Feb 2025 22:23:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26adf19273ff38a41503b067a8d1c5a35d4048e2291780e1ffa91def36425f6a`  
		Last Modified: Fri, 14 Feb 2025 22:23:48 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:b00591e00a263982885b0bee54a5d7c27ebcf5249fdaa334c51fc223467aabf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90bf2a0d811c39c7759e43d4257b01711ffdf36fa3dceffc397887cc7f8fa9d0`

```dockerfile
```

-	Layers:
	-	`sha256:c19f26a228bd4be6de3aa9d8196866405d54f8bc38d014c8f26254efe16ae04e`  
		Last Modified: Fri, 14 Feb 2025 22:23:48 GMT  
		Size: 79.9 KB (79878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5a1704deb4400e22af6abe356817cdee187689b0cba34988ce227508adfd78f`  
		Last Modified: Fri, 14 Feb 2025 22:23:48 GMT  
		Size: 14.4 KB (14433 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; 386

```console
$ docker pull spiped@sha256:61b83f6f4da433231db95db1a13fe86dbe85aaecde12dcb9a669f0b0ed0b6e84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3593051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b68ea95baf750c2a2749ec794c8238c510e5792dc8857ed4a3645d071f394823`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89de02b79b34b2bc491f8c7e8607233cc124ed19295cf456e64382e5afc72fbd`  
		Last Modified: Fri, 14 Feb 2025 19:11:58 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff1d235c70003f61e0de885229553d72517e82d7f45df6d561b480b2cd9c5fc`  
		Last Modified: Fri, 14 Feb 2025 19:11:58 GMT  
		Size: 7.9 KB (7914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68a0453a1d3c0248fee96f306a8ede9aa3d7f2dd02652a8dbdff1b0d8c9438b`  
		Last Modified: Fri, 14 Feb 2025 19:11:58 GMT  
		Size: 120.1 KB (120130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e021c9b7ed20e7390deef74c89a7a5540f6309865137308f9a80ac607be260f`  
		Last Modified: Fri, 14 Feb 2025 19:11:58 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2872beb154170ecfc36e7b32d8019cfc1e29a60d26d251929d28131277a7fd0c`  
		Last Modified: Fri, 14 Feb 2025 19:11:59 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:4c3f4670bd80d3c0136a64e6f27ff285948a413faee904ef1c460b8f51d4e516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8c5f2d723a731a066cf77f9a59824e65134fef732e62678056b932016e17282`

```dockerfile
```

-	Layers:
	-	`sha256:b1e174fd16318b9fb1190150ba833822f30825a45606ea9af9ec1723ce03867c`  
		Last Modified: Fri, 14 Feb 2025 19:11:58 GMT  
		Size: 79.8 KB (79797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86e4a7deb35e498340a41c762c8316785005a9ab4e93a2ab0a677fc623e721fd`  
		Last Modified: Fri, 14 Feb 2025 19:11:58 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:0763e833f3d2e767ad7c1ab64d3a1778d9543cffbe2731d7f8c40bee27d44a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3696292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1cde70893ef4a0b94f4624b6bd8ea6a51522d65faf50b2646cac866d386dafe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22ff6ba800883c9495b3d17b7735935035a83bdb153e380d5f5f6c80c3573c5`  
		Last Modified: Fri, 14 Feb 2025 21:51:56 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77eb59aefcf51d96da7771cb0671fa43ebe8e636326ce4db947ff446ea9b4eaa`  
		Last Modified: Fri, 14 Feb 2025 21:51:56 GMT  
		Size: 7.9 KB (7917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b657e1255fd2cfb228ed06e75846652368ff0d80307f8b278c3db5e5558f4f64`  
		Last Modified: Fri, 14 Feb 2025 21:51:56 GMT  
		Size: 112.6 KB (112646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1de73da0d337b9f7fd4e60cf9b67d3592f9e6f6f539421800b167a2735f1bdb`  
		Last Modified: Fri, 14 Feb 2025 21:51:56 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ad280a5133fac353984bead0c9962cf3a9c94714d7806a61832de902c8e929`  
		Last Modified: Fri, 14 Feb 2025 21:51:57 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:522f73a6a1f1e955300602615eb9a993897959108be79c09d235f1db5e488940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 KB (92255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f95185cb2bad6bef09c576b8e4d9d0bf6563783c294a92e69f28b758029f2ac0`

```dockerfile
```

-	Layers:
	-	`sha256:eb306f89b50101c069df46fb92b19620767f2503887c596aedfc415f347a4246`  
		Last Modified: Fri, 14 Feb 2025 21:51:56 GMT  
		Size: 77.9 KB (77905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c821af9afc609e7780dcfb284627dd581cbede4a66c24cc04b41f590c6244531`  
		Last Modified: Fri, 14 Feb 2025 21:51:56 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:4e7de8f9709ec3d17502bc8bb28f682390ca0f28540c21c3a3af3d7c341dc246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3459539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:504149511c6ccc2b6171cb52f835ea33310f60a13cb4f1217042ba7b30d26964`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c30567d05b83d280c92f0fd67f2111b6e24b0ed19d33f47a59b9ff4de364a64`  
		Last Modified: Sun, 16 Feb 2025 05:54:31 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d0963c5b0ae916eb236c2459006edc9e233988196970deb59739005856241f`  
		Last Modified: Sun, 16 Feb 2025 05:54:31 GMT  
		Size: 7.9 KB (7903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92254399fdbccb7d8366a87f97833ee67c515bf8d17be08064a3b25323ec019e`  
		Last Modified: Sun, 16 Feb 2025 05:54:31 GMT  
		Size: 98.8 KB (98811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4b70370fbe28ac9fa59252adef103c1e801b11b4282a7836f323b6f9cfbbf0`  
		Last Modified: Sun, 16 Feb 2025 05:54:31 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421ddf9c5739ee7f0969aac39a6c858cd81ff02ee5f765c215cda1d7404f7ee4`  
		Last Modified: Sun, 16 Feb 2025 05:54:32 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f9cc83e697345dc797170082bb5f58796e3c4247db4a7e9dc9a18c5f5d770c1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9082f8d0a7bf47b624f56e71a3e3aa17d3af84359fece9dc0ba70c14b635f7f5`

```dockerfile
```

-	Layers:
	-	`sha256:e79532d7edd009e631ef81e580e98cd57bd38a27218b471ca6d59658abf18da4`  
		Last Modified: Sun, 16 Feb 2025 05:54:31 GMT  
		Size: 77.9 KB (77901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5a81928e2faccb215eabff958751f6bd93127a2016536154fd6142ca42fad06`  
		Last Modified: Sun, 16 Feb 2025 05:54:31 GMT  
		Size: 14.3 KB (14346 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; s390x

```console
$ docker pull spiped@sha256:de25b12e766fe57e24177257227c53d5a27fc1a3ca4abe48e8bc60e0351bdaef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62cb095475057abb702522c9d705013168c8522d986f39b9047739ee6efe16b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a28161d111a002ad388fefdd709f7bb67cb61071bfdfa7960202816d14c2e2`  
		Last Modified: Fri, 14 Feb 2025 22:26:10 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30984a12769648824acad7e1386b7ba7193bf81929e37f44ce5f3c04f82acc6`  
		Last Modified: Fri, 14 Feb 2025 22:26:10 GMT  
		Size: 7.9 KB (7915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b5b85eee8dde04ba3dbc50eb3b644d79d18255b1eb4dfa5c888403b0ad97cc`  
		Last Modified: Fri, 14 Feb 2025 22:26:10 GMT  
		Size: 96.9 KB (96918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8860fa829f189bb5e960d5036162d15a1aac72e9ce8bed6c40b68549752c2199`  
		Last Modified: Fri, 14 Feb 2025 22:26:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb23aa9487acbddced4252bb38b3510de48d049a3a347fcfb6b24f40c9ff730`  
		Last Modified: Fri, 14 Feb 2025 22:26:11 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:2065dca98493b203898ab91ad7de40fb703351116ab3bfc12c9a52026ce6c13e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f932f07832d03eeec80862781aec2cb3efb7c48fadec873786bd1c8af939e6f5`

```dockerfile
```

-	Layers:
	-	`sha256:8b919ae512d1430c2c7488ea884c9bc49e2ae21b5170043f2a370c90e9af6c60`  
		Last Modified: Fri, 14 Feb 2025 22:26:10 GMT  
		Size: 77.9 KB (77871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddf9c418603cd0c1fdf650dfd352e9ae11c6eec907de4024a31a994019249053`  
		Last Modified: Fri, 14 Feb 2025 22:26:10 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:latest`

```console
$ docker pull spiped@sha256:fc1f33ece364de511a2a44f0539a7716bea1ec0953fa91c42a303a66cd55b77a
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `spiped:latest` - linux; amd64

```console
$ docker pull spiped@sha256:c19bf364bfa9b01e7f25e85f3c4182faa24af4712929de98e36e6a0b7edfd4cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37066454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbfb718114afb7be4711e5fb0bd240c9dd0a669ae1b48d93e3426532a35ba4a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9e666ee2080d653e24746cfb863a5ae3e9a9b21760fd38c5b68d6dd7b3c585`  
		Last Modified: Mon, 17 Mar 2025 23:13:32 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed2bd90f46aec7eec2a2c77a4bb8df89a0a3e132b6f270532ace804fc51464f`  
		Last Modified: Mon, 17 Mar 2025 23:13:32 GMT  
		Size: 2.4 MB (2401370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:993eee5dbd6de6d47b0071ac15523a45b6a8afce9d50daa61807c346f47c266d`  
		Last Modified: Mon, 17 Mar 2025 23:13:32 GMT  
		Size: 6.5 MB (6458678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbd4bf8003cf0865eb03cc5f3d90f07d682ef429b2ac0e65b94c6f010d77b47`  
		Last Modified: Mon, 17 Mar 2025 23:13:32 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:993319058db4392c9db4ba00cbfafbbabede0f3d777fde6728dd4eb483b42ea0`  
		Last Modified: Mon, 17 Mar 2025 23:13:33 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:4e76634ef610cfc556713c4be1a31147ab325ba6832e229407f56e6e02388d0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3530884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4872dedbd739de53112c09fc8399226956b43076779518fea2f0ab2b9795410d`

```dockerfile
```

-	Layers:
	-	`sha256:5f30ebd653ca5651357a3623b460af90e8777573dba62f3f6d6f541434841741`  
		Last Modified: Mon, 17 Mar 2025 23:13:32 GMT  
		Size: 3.5 MB (3515844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b84b0482b1865ead9d5b18a7dac5921be9c7708b96d0604ccc0721d114d442a3`  
		Last Modified: Mon, 17 Mar 2025 23:13:32 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v5

```console
$ docker pull spiped@sha256:7fa569baa2e4571917dcfbfeccc8243ff376678076033123e3833b11906156f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32886160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cc3d47e814f4faffd8aadf598cba98077df9c5e04f8ba3eda699ce802846b01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1740355200'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d8a77b84d73cc90f2bbd622ec970d928c4f14e4be51927c88b7c15b7b6772382`  
		Last Modified: Tue, 25 Feb 2025 01:30:58 GMT  
		Size: 25.7 MB (25740630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8e82324f9ed6ef92c3805276fe1ab8fa8bdd8f407015897c22f32e81556448`  
		Last Modified: Tue, 25 Feb 2025 05:15:19 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18c80389cadb88242cd228219aeb9461304257e925f8811fcbbb470bfd81fd0`  
		Last Modified: Tue, 25 Feb 2025 05:15:19 GMT  
		Size: 2.0 MB (1997208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb256a4313e4774f05ba257deb90ef81ede34bcd9b0d362197570f93fbcf8ad9`  
		Last Modified: Tue, 25 Feb 2025 05:15:19 GMT  
		Size: 5.1 MB (5146780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c3479c48b0ffc4461c5733c985e0bc4325898f27e1607eb84694e696f0ea8b`  
		Last Modified: Tue, 25 Feb 2025 05:15:19 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ec20e1f9a518c4b39a8f5c13cdae21c5d3b60596708602f864327841d36a2c`  
		Last Modified: Tue, 25 Feb 2025 05:15:20 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:3f047eca507cd403c6791648f7c48d66b9349872175c945885648e29b26ce926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3501504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58ec476a13815a2e160b782fa4020274a1005169e66f37c71bd644af3012f18e`

```dockerfile
```

-	Layers:
	-	`sha256:73ec23c96dc073e6f666bf47b1205eb39f3ac9ed516c86358767507b06a4cc1f`  
		Last Modified: Tue, 25 Feb 2025 05:15:19 GMT  
		Size: 3.5 MB (3486362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f8715208bb569facd33c761f2a66848a951deb8cd9e5e1d8777c513a99cbc17`  
		Last Modified: Tue, 25 Feb 2025 05:15:19 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v7

```console
$ docker pull spiped@sha256:99b05b73d0fddf2fa852924722f7219b5185938cac147b249ca64681a980e754
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 MB (30664848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6d3b4bd3bab0abe7d81cf37c4c4a6dc75201aaae6e4f9085f40f01b6bf54d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96913db2d7bf2a45c109be6aa196dc22884e8cccc1cc3b2a39f613a1b90d0943`  
		Last Modified: Tue, 25 Feb 2025 07:02:33 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2566e9b1179e5c8fd6832a19e6629a6862e2021b9fe8d593dca6687eaa0eef0f`  
		Last Modified: Tue, 25 Feb 2025 07:02:33 GMT  
		Size: 1.9 MB (1855566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef718bd99e2a7a5d409e423e94cdc1dd0cbde16231d4c9326956ebeb917a30f7`  
		Last Modified: Tue, 25 Feb 2025 07:02:34 GMT  
		Size: 4.9 MB (4888006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:695edf7c1f3066970e1e3fbae552988aa33f3edf00607d0630d75f52d2e3a950`  
		Last Modified: Tue, 25 Feb 2025 07:02:33 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b009750be7193bc571d7670a73753f454748ca939d25b521e360b5d5c169b91`  
		Last Modified: Tue, 25 Feb 2025 07:02:34 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:893aebd041e27850e114022d592b5dada21e4a35fc0fc0dc4dc7b6d2ab38082f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3500995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec20510c844f5ca50a521741419fe9c064c9892854403176caa8c38145aafd4d`

```dockerfile
```

-	Layers:
	-	`sha256:a5f92c4b0879f8bb8005a8f0e129a938fbacb2e0f6f57d6a84bded5d8e2f203a`  
		Last Modified: Tue, 25 Feb 2025 07:02:33 GMT  
		Size: 3.5 MB (3485853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a94619fd89e6e1f45e5167c17cc1ee967ead21b2a6e15b6f48f1724d8d5671ac`  
		Last Modified: Tue, 25 Feb 2025 07:02:33 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:db53a8c274356cc5da81ada07bb47c61deeb780565f3a80bb603f04a305939e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35788124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:798f3cf34b0f1cc65a81a2efa6db7b05e25dbf4b2535aac42ffb89fb5710c962`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67307fdcfcd65a772010b76ebe296081d6a488e144cdcd1c9d0781cc8f6ea3b6`  
		Last Modified: Tue, 25 Feb 2025 05:20:43 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4da10b03c1db04ea42046a0699a6547ea8fa47cce175e19c4af8db06fbdef1`  
		Last Modified: Tue, 25 Feb 2025 05:20:44 GMT  
		Size: 2.2 MB (2247031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d214314c22c6b6ada301a5df4aab4c5742554fa40efe4ca909ee898af9db44`  
		Last Modified: Tue, 25 Feb 2025 05:20:44 GMT  
		Size: 5.5 MB (5491125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfaaafc3dbcec82ce792cdae6d39e35f6417a7e075534a44b672555735909163`  
		Last Modified: Tue, 25 Feb 2025 05:20:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aeb2d44a802d2f56e52ca4c03efd33ef782441e341d59963b50cc7942cb2665`  
		Last Modified: Tue, 25 Feb 2025 05:20:45 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:1aecc6411bc714ed9b10aa0749e161fc320f2db0704eebb6d7a7517b37e10e9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3502234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a40cdb974e39defc6d4761b60a63bbcea7e9df48f328d4e44582a872027e5bbc`

```dockerfile
```

-	Layers:
	-	`sha256:9bf2b1992699b289df18732bc29ebf544c16efa4f5060b1c01fe821c546fecb2`  
		Last Modified: Tue, 25 Feb 2025 05:20:44 GMT  
		Size: 3.5 MB (3487060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0003b97ac68aada1c31926eb0388cf5715e3c1e094b441d7bd4c2b82fbc6f43f`  
		Last Modified: Tue, 25 Feb 2025 05:20:43 GMT  
		Size: 15.2 KB (15174 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; 386

```console
$ docker pull spiped@sha256:8c3d5a5c56abaaae7abf82cf38241e9b7c8f004a26ccda6ba2257441f3bda2f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37546405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8fd46d4842028eedc1776850f7dd150baf9836168006deed35db9cbbc2e1be9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839e731aef1461390a040cebeeac983c7d9bb1cf3a1b92df974e5d38ab6a5a09`  
		Last Modified: Mon, 17 Mar 2025 23:32:55 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c778ac50739d7d7b86008e98fd5f789cb2cb3987389237d4e6b51d38bf17f9a`  
		Last Modified: Mon, 17 Mar 2025 23:32:55 GMT  
		Size: 2.4 MB (2398675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6d38a505eac9eac7a34554d9c99811feff3b705f79cd6d662e56bba0822a01`  
		Last Modified: Mon, 17 Mar 2025 23:32:55 GMT  
		Size: 6.0 MB (5956664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1ee1056d4f06ee344237cf71c7c1469bb31a29a9478dfa3b259dcc62aaf042`  
		Last Modified: Mon, 17 Mar 2025 23:32:55 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d87efdd8714801b774cf86b2261e9e30d73720eaab82e08cf72d42728094ce`  
		Last Modified: Mon, 17 Mar 2025 23:32:55 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:e35f402ec773de33f2d781228239089173b113441dbe92a071096d943f07e015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bf69b249922ed757f9478e3e2be76cbc4d31b306002dfb5e0df0c6bff530832`

```dockerfile
```

-	Layers:
	-	`sha256:e5a700cd41e3b54827acfc8a7168de1917ba898044ee19a4e6d69de32f5453e6`  
		Last Modified: Mon, 17 Mar 2025 23:32:55 GMT  
		Size: 3.5 MB (3509771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd2af87232f9a80fac7c822128970a4346e9c20ba22b5a1fa0c4c745e534aee2`  
		Last Modified: Mon, 17 Mar 2025 23:32:55 GMT  
		Size: 15.0 KB (15004 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; mips64le

```console
$ docker pull spiped@sha256:f588c7961b2391e29412043bb650c5373ef0d58747e046c824e4aa600b0a3f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36149433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59dcb4aa75e3de41c2a2a75f202d0461f011431c4e2e006675a7821dfd2e2289`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1740355200'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:1851efe37d59b19d5c7092778464657e31dbfae35874c19fb94fb95542e2fba7`  
		Last Modified: Tue, 25 Feb 2025 01:30:49 GMT  
		Size: 28.5 MB (28493681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d443002accadcbf61d00cd6a4ff2148154506b88bafd1824e60d166574549d8a`  
		Last Modified: Tue, 25 Feb 2025 14:46:42 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6876c742899903aae4cab3858c4f7748abc5cdd72cd13499bfd7a31051a866d`  
		Last Modified: Tue, 25 Feb 2025 14:46:43 GMT  
		Size: 1.8 MB (1841111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27741d3453c8dd83a2792eb7f7855412b2783f3aefd7364c79ed196963f092a5`  
		Last Modified: Tue, 25 Feb 2025 14:46:43 GMT  
		Size: 5.8 MB (5813094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9571b92a553f23ec240639ff8c664c5fe98f9ccfb0ad4d9a0e2c11ff8659f682`  
		Last Modified: Tue, 25 Feb 2025 14:46:42 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd4e0b5385ab0445f22fdaaa772ea7005b535d4a354c0ee3852c650fa312b1a`  
		Last Modified: Tue, 25 Feb 2025 14:46:43 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:012cb3dac4ad50d2b5c46601ed61f62a31238587e2632167c3a5b6f339bdc6ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eb9ace30b83120dd844131c6d0936723af680f21c0d081e5e8d98ec0dab8afc`

```dockerfile
```

-	Layers:
	-	`sha256:39a263ac3a5b1feee0dbfba1c9827d227e5a7df25a84e4393b5b59951314b086`  
		Last Modified: Tue, 25 Feb 2025 14:46:42 GMT  
		Size: 14.9 KB (14897 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; ppc64le

```console
$ docker pull spiped@sha256:2d56269c6465cc901bc554cfdb03676cc554945c82b352d308107f5a5bbb8e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41076744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5dd5e4a7a596f710398a998f1c2f30ecf1215b4c0cc62406e61e00c148d721f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff7dfc5ec19a2023a35f359183c5f47a6cc2262506bdfa96caadaea3436edfc`  
		Last Modified: Tue, 25 Feb 2025 04:17:33 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd1c1349f74886a6045e95ddb2858cd4bc0c52f426e9ea28503f764a99b7435`  
		Last Modified: Tue, 25 Feb 2025 04:17:33 GMT  
		Size: 2.6 MB (2582101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c259b563b886cf3310babb5e8c89e8f4d2ba6c99db9282d58b4959d07be769`  
		Last Modified: Tue, 25 Feb 2025 04:17:33 GMT  
		Size: 6.4 MB (6440788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be98953031df8386412e13d3ba09a2448f2f4d9cc5a4be9be1d6767749767fd`  
		Last Modified: Tue, 25 Feb 2025 04:17:33 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336fe8e170289066f18894050bac32156f5d8addae22832618a348398f626ad6`  
		Last Modified: Tue, 25 Feb 2025 04:17:34 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:3c893d4c21851d0dead8263c087e5f1ac53a0397dc3b928b37e088a93f846687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3516589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c075768c2027385e1bc38708b3b1fd535362325c6d869c81800c1f7da1922e64`

```dockerfile
```

-	Layers:
	-	`sha256:8219b097b6744e8b7f9da40627c847256d7a19becc5880ae438b74855641b489`  
		Last Modified: Tue, 25 Feb 2025 04:17:33 GMT  
		Size: 3.5 MB (3501501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8ddb3cb5465f4081c0f39d526cc6e312f4a46ef9614ccaf09c85e70f8c574ee`  
		Last Modified: Tue, 25 Feb 2025 04:17:33 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; s390x

```console
$ docker pull spiped@sha256:263a41c61c6e51a81595bf21d29b293dc8ef1dc6db31846a87528016f6f231c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34326809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:731add486ad8c841f4ee0da0bdf079dd4fc9d95b787f675576b8664cf34ceea6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6d4d169c55c2ee02478b6705c4ba9e6795bffbbb872a22adfd95fb2484f2e85c`  
		Last Modified: Tue, 25 Feb 2025 01:30:03 GMT  
		Size: 26.9 MB (26864838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a09f8852f4de85ce593ec49e5bb2cd625906f3d110243cb6a07a435ebff3c3c`  
		Last Modified: Tue, 25 Feb 2025 03:55:09 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d089fdda46bdb7be319ceec736408cce334720e9f43d43f4f6f571796b8c71f0`  
		Last Modified: Tue, 25 Feb 2025 03:55:09 GMT  
		Size: 2.1 MB (2068731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d178c00425fc4a8b273a41abd4d42f17485cebac65dccb7d2d34bc0f2236a3d`  
		Last Modified: Tue, 25 Feb 2025 03:55:09 GMT  
		Size: 5.4 MB (5391698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ae414cbce0fd75ff49297b77b90536f6edfdbbf9f72143191f2e2f029dc792`  
		Last Modified: Tue, 25 Feb 2025 03:55:09 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19fc135aabe22a7b2f284fdb665b918bb0b3ab9e28745e68ebc4f8729a1eb83`  
		Last Modified: Tue, 25 Feb 2025 03:55:09 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:4338e2c984858a2ff1b2e2c98b9845da59713878e3718b28fc7bead1734e3e22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3519058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c9a1890740bd8c0586f0f8c6feeae6678663abeb76e20e623ec8ed7e47e5765`

```dockerfile
```

-	Layers:
	-	`sha256:b95d1ed970c8f6578ef0c5440e8984ce588648a047a69f64ccab2c2251305422`  
		Last Modified: Tue, 25 Feb 2025 03:55:09 GMT  
		Size: 3.5 MB (3504018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6033e6dc86c10bc0920271bace69a7abbf13198adf934992a0f16c0e71d8a2bb`  
		Last Modified: Tue, 25 Feb 2025 03:55:09 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json
