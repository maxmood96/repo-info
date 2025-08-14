## `buildpack-deps:questing-scm`

```console
$ docker pull buildpack-deps@sha256:a1b0d92043263a3cf82c0d6401d823dbf034d06b6336ad46153f9a59fa7b8d38
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:questing-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e94c914c14a9cbcf15d8641726807bc7ed5ea02421b7a8c55ed2ec31df8b7cf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.6 MB (98612894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31998b5c77ddebcf3e80d6954d1cc1706cbe35f92fec1e9d819a1e334266afb0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 19 May 2025 22:25:54 GMT
ARG RELEASE
# Mon, 19 May 2025 22:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.version=25.10
# Mon, 19 May 2025 22:25:54 GMT
ADD file:17cd460f059360977af8d3a00489852009c22a41f4352f2ba85943f0f8c5f41f in / 
# Mon, 19 May 2025 22:25:54 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3b9d892b6aacf4b0c1cf535d30918dc2256e0c2f52cc1d37bee19067663cbaf9`  
		Last Modified: Tue, 12 Aug 2025 17:03:12 GMT  
		Size: 29.7 MB (29699735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf6521f3b67e01b294cb3de33f7542134a1555d8668193478d0e42ffeda8ade`  
		Last Modified: Tue, 12 Aug 2025 17:23:37 GMT  
		Size: 18.9 MB (18862507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e95df3a987333c68a6d923628c33ebeb8e18231c26d40b3d9abe5891f18791c`  
		Last Modified: Tue, 12 Aug 2025 17:52:46 GMT  
		Size: 50.1 MB (50050652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6169af7a27083a775bddcbf32a26a342c82251dd4cefffe291083e23a8e1dfc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5440983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fc4877ae7b3a7a47e1ba2aac6de8565623534b12ffabc681e1674a5b2cac07a`

```dockerfile
```

-	Layers:
	-	`sha256:ca1f4da16e20c351205bc0ea0a9c4e6d976e2a17856b8925985d03049eecb1d5`  
		Last Modified: Tue, 12 Aug 2025 19:21:01 GMT  
		Size: 5.4 MB (5433659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2da11c6d3661867835e2176641fb0d2c4b77a5522ab6c1fe7b87cb064bd34b9a`  
		Last Modified: Tue, 12 Aug 2025 19:21:02 GMT  
		Size: 7.3 KB (7324 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d654854adc16691cd6b5978e606f3e5e649e9ed70192b1474e69f7504e325b88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.5 MB (97530977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:747d4c32c7addd723a160acc96328a9bb8702647641dcfe0094a851f6415a39a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 19 May 2025 22:25:54 GMT
ARG RELEASE
# Mon, 19 May 2025 22:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.version=25.10
# Mon, 19 May 2025 22:25:54 GMT
ADD file:9eed1b2293ee9b1a3f538aceaac3ea32a998f61f054dad9cd5a407828bc5e7fa in / 
# Mon, 19 May 2025 22:25:54 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0d7bc1e0094544c65656ef653b3c67a22bb857cf01de93e24e36a5b8bd9c6839`  
		Last Modified: Tue, 12 Aug 2025 17:03:09 GMT  
		Size: 27.7 MB (27736612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d602962dce0a4ffd02b7128b627e79af88041418e069c243e79a489d2c76cc9a`  
		Last Modified: Tue, 12 Aug 2025 17:24:45 GMT  
		Size: 17.3 MB (17259013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af33432f0724121e962e4b411da290ccc76a6b8c0919ab48a491d6134ccb2b7`  
		Last Modified: Wed, 13 Aug 2025 17:21:43 GMT  
		Size: 52.5 MB (52535352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:415fc15458cefdeeb9ea9fa240a47a4e27a35fc96a07c791047638c3fa1da4dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5441536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf92cf90e4413fe93c3ca62fd448910794e2fcc1540f56c54360f52b14788d01`

```dockerfile
```

-	Layers:
	-	`sha256:30987e57edd44601679f57942a559f7cc918508a039e8b2916160ee6b6504cb7`  
		Last Modified: Tue, 12 Aug 2025 19:21:09 GMT  
		Size: 5.4 MB (5434152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2530cd7d274704de171c77efaa44fad7397ab30c2ff0b2857a5567c4b356461`  
		Last Modified: Tue, 12 Aug 2025 19:21:10 GMT  
		Size: 7.4 KB (7384 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4ec631d703a9c4adca0f8d3a6f0f488dfa0f30fe0575a929282c35609acde087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.5 MB (97477178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7614cca0bab57b8aea29687992bff0d9fc7b3e7ff26a5d37ad716a5af0879984`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 19 May 2025 22:25:54 GMT
ARG RELEASE
# Mon, 19 May 2025 22:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.version=25.10
# Mon, 19 May 2025 22:25:54 GMT
ADD file:ec3f48e621d9128ce28e8aec63d50c4c4eefc59528b99116bbc3032f4279f5ee in / 
# Mon, 19 May 2025 22:25:54 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c6f3bc6961ab41704f6454c7be252d2be9e9153165b095e56dea5e0112de7753`  
		Last Modified: Tue, 12 Aug 2025 17:03:14 GMT  
		Size: 29.3 MB (29314444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47763b1514857655ffbc66a9fedccd790dec27127100e6dbf9ae3a5fdc7b6d8`  
		Last Modified: Wed, 13 Aug 2025 17:21:13 GMT  
		Size: 18.4 MB (18384151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628b6434ea47d356ba7c65e3f77d6bb7f6f2d54d59b3b4d635243a46a8e69e3e`  
		Last Modified: Tue, 12 Aug 2025 22:16:19 GMT  
		Size: 49.8 MB (49778583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b17fbfe712b90a804282a9d067434c29ebe604a30ea8cf00b015e748f12ee74d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5447449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a7650c7feed14f80e7a4c36dd9dc04a479ff5af6063b3fb6353dbc2f99ef33`

```dockerfile
```

-	Layers:
	-	`sha256:9b17304e30aa26e6ccd15d0e6b05e5c3de99ce5f3f9fb2da8b64b69d88cc3d0d`  
		Last Modified: Wed, 13 Aug 2025 01:19:57 GMT  
		Size: 5.4 MB (5440045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70272f3cfc80870c3056ae7a2c59f63cdd9a7ddd4a38349e1befefe36f3c9900`  
		Last Modified: Wed, 13 Aug 2025 01:19:58 GMT  
		Size: 7.4 KB (7404 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:6d15a3baed7610120d4c313f857f703739f6880f6fe404f319edead5afa3f89a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 MB (110562192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c44935173af5b7f0e62ecdc575ca811dc68f89a68eb6f9cc9100d071742789`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 19 May 2025 22:25:54 GMT
ARG RELEASE
# Mon, 19 May 2025 22:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.version=25.10
# Mon, 19 May 2025 22:25:54 GMT
ADD file:566d1fae557135e37d75df659c267bd6a62cf94b1fcfe7e157578d9270ef463a in / 
# Mon, 19 May 2025 22:25:54 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0b1109ae8bd2c2ee8f31117236bd09c15587a8d6ba7a611f16c4200c2bb761de`  
		Last Modified: Tue, 12 Aug 2025 17:15:59 GMT  
		Size: 34.1 MB (34111991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eca0501624351fb3456fb0392bb33c5140287cc91e607e55eed9b0d1cd8846d`  
		Last Modified: Tue, 12 Aug 2025 17:27:55 GMT  
		Size: 20.7 MB (20745823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a06657384bb754cb4b3846f3caa8a12bcc375aff96c2b369a2a25369b0d022`  
		Last Modified: Tue, 12 Aug 2025 23:18:47 GMT  
		Size: 55.7 MB (55704378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:745c509d4d2eb183084fedc2071b3e67e6aefb0eab60653d3547fcb78f128382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5448068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11f4786efb8c59f18e27f39c4cc0567dc3a4c55f0ad9aac6482f21e4d1c0fde1`

```dockerfile
```

-	Layers:
	-	`sha256:6f37aa354e30aba6df685159a7044499f7145290142975daa2e9d056013e740e`  
		Last Modified: Wed, 13 Aug 2025 01:20:04 GMT  
		Size: 5.4 MB (5440712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5c4bfb28c20fb567c8e2f633ddcf3efe2320e133d58be7493007679f544ab4b`  
		Last Modified: Wed, 13 Aug 2025 01:20:05 GMT  
		Size: 7.4 KB (7356 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:54a3f5e95941eeac8712522c5c03b4f9c5db957f5607ce65de032f22b959f0c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.1 MB (102114749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d7d3b91c04d026961b69a0b1650a17f000239751ec455b485a3e33c541e721c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 19 May 2025 22:25:54 GMT
ARG RELEASE
# Mon, 19 May 2025 22:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.version=25.10
# Mon, 19 May 2025 22:25:54 GMT
ADD file:2ad5f91fe5edd35a8a0cb6ec99904a35771f2b8a0819b888cca27bd2b8edc998 in / 
# Mon, 19 May 2025 22:25:54 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c765da7735337fafbed911e71485d7f0505e50d1941beb7fa962494422b6b9be`  
		Last Modified: Tue, 12 Aug 2025 17:03:53 GMT  
		Size: 29.6 MB (29618719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b53c981ca1715af0d0448a048d0a4642c6a7becf08354f007f4e1da1b9569b0`  
		Last Modified: Tue, 12 Aug 2025 20:19:20 GMT  
		Size: 20.9 MB (20949219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b53944a72c5140ac1e0979538c80a60692cb4b9b098e1921d41485efb62ee5`  
		Last Modified: Tue, 12 Aug 2025 18:44:14 GMT  
		Size: 51.5 MB (51546811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:719711c8d8c566349f8cf688d1d3f1d7633514aefb68b01c618a89209825bd37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5442522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecb9391c7c133f1fd4db56d780dd9a5cacd5854295aba34991f40e48abf6aa68`

```dockerfile
```

-	Layers:
	-	`sha256:068841860fc1ccd95e0a1a5bc0fe092ee8d877cd2b4a3e0b489430a27ce69398`  
		Last Modified: Tue, 12 Aug 2025 19:21:38 GMT  
		Size: 5.4 MB (5435198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82cf10f46a38c6f69739a3f3ae378d1a02c9e7ef2ae69e4e2f813c4a3e17f33c`  
		Last Modified: Tue, 12 Aug 2025 19:21:38 GMT  
		Size: 7.3 KB (7324 bytes)  
		MIME: application/vnd.in-toto+json
