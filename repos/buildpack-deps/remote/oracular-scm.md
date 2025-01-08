## `buildpack-deps:oracular-scm`

```console
$ docker pull buildpack-deps@sha256:0325cd014a1561ff9039b66c2bf45acf5981fde10dd02e119c30705e51c4b862
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:oracular-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:563e8451c6e61acd1253e9387da1481be89ae5e02a0111a8fc481ece758ea0eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92466770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71d68ca44aa08186ffc80697404b975b0f1762747a215809a8a9f250099ea38b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:08360137caccff53ccad4b814b2e19f27aa9fe2a71175550a7f6b13fe243924d in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:31734b193a814b7d6f96f0d11a89c942ca61ac79d819105323c548bf31f98613`  
		Last Modified: Wed, 08 Jan 2025 02:14:24 GMT  
		Size: 30.6 MB (30601312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb3a0dc114c54fd18d42d481f5d85eb84000d5cd297bd2f753d1290eb36719c`  
		Last Modified: Tue, 03 Dec 2024 02:29:09 GMT  
		Size: 15.4 MB (15374140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64ddd91578315b54cf47f01baf6ea302d702c1bc46efefdcad51af4f6a7812b`  
		Last Modified: Tue, 03 Dec 2024 03:17:12 GMT  
		Size: 46.5 MB (46491318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8ba9fad56bedf47846b079812c8a6d4f47a1dc796f1dbccd5a2d1818033f9fa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5097877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f725ce812a005ebd7092e7623bfe9c5a339b6bd4da22634dae370ff500604947`

```dockerfile
```

-	Layers:
	-	`sha256:c23bc9c092c296df444d5a1fbe7d557d5c72492a03d7b3b366f8a8106b1c9c9a`  
		Last Modified: Tue, 03 Dec 2024 03:17:11 GMT  
		Size: 5.1 MB (5090553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ba7f94c1ac96e0c4b0ea537df4662194ce9f2b029b822a146f047255b3af022`  
		Last Modified: Tue, 03 Dec 2024 03:17:11 GMT  
		Size: 7.3 KB (7324 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f35e17de918b1ab011fb1b0334a6c8c87fff4b4a798a2a2dd80bb307e39cdb6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91070800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27344efd4600537f2d0179a82ce6aa58a2d6a24a8cb1bc5ca2b9f675b5ba4d8c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:5cf848783aed3abcaefd540a7a70f443ef2bead6c50d01e0a72cd1aa6f542081 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c553618cfeea14cb253bd7777b2e3299019b3065e1cb073744b43353379582a7`  
		Last Modified: Wed, 20 Nov 2024 04:18:39 GMT  
		Size: 27.5 MB (27546971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a00677e72221e7026f8e6b0ed5b47e7316c84195a5d85d7c2cf005d741e670`  
		Last Modified: Tue, 03 Dec 2024 07:40:05 GMT  
		Size: 14.1 MB (14060900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c52f0d85713a2f01f551bbf8afba0de5917d8a73a492b3fca6575c2696d83eb`  
		Last Modified: Tue, 03 Dec 2024 17:21:00 GMT  
		Size: 49.5 MB (49462929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:321e47836c05fbb02e1fd02fcc1ddc2c3c9659ace387ed72c88a22a232eb575a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5099237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d40379b9a864667266d066d886c9bcad244b1e2b00a22868aeb7f34d7b32bef`

```dockerfile
```

-	Layers:
	-	`sha256:1ac741d22a8e2ee37128ae932b86c198778eea3fd1c9530edaa933db1bd2bcdf`  
		Last Modified: Tue, 03 Dec 2024 17:20:58 GMT  
		Size: 5.1 MB (5091853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86ff1a3ca795c61cc4e63a408b81086ade9a98c28eec81011f6ef2d2f5a94d23`  
		Last Modified: Tue, 03 Dec 2024 17:20:58 GMT  
		Size: 7.4 KB (7384 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:cdd5ac19c22ca37622957e9f58856f47133d1411fe3dfd34e5351a0d0fb7618f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91855613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8100dbfdf0f4d4dff2d6d2e852b149139fee0a29c4411415c911d1f1751d4e6c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:11edc0b5b8a0810c86ff8de1ece47e84856118afa9f296152b12c0bdabf33154 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6d229850a7784435237486a1406ffb5a4f0a4ac3b993928d18b30ad6853c6845`  
		Last Modified: Wed, 20 Nov 2024 04:18:26 GMT  
		Size: 30.3 MB (30284785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c08bcb2cbebb6d9db3a5ad2c52e975d21aa32088786303f6c521a0bb1f93f0`  
		Last Modified: Tue, 03 Dec 2024 05:41:40 GMT  
		Size: 15.1 MB (15147474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be5c9e4ce5805ad177f3aba8a70b5f1255051eb50b349f3819d9ee550186986`  
		Last Modified: Tue, 03 Dec 2024 11:54:23 GMT  
		Size: 46.4 MB (46423354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:247fbd221ad5fefbf18c52d8696177a8e67b46e00e7d5e256a9bb950b590c27c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5105157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58c6b74132fb1f57a9d10c9981fefad798e3ac9551eafd4bccce198df20b4cea`

```dockerfile
```

-	Layers:
	-	`sha256:5b41ccdf769d6aa00d98c9cdb9bbb11353d81d3f89b2d37beceb76d737d5c56b`  
		Last Modified: Tue, 03 Dec 2024 11:54:22 GMT  
		Size: 5.1 MB (5097754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:573bf2b358841fdfccaf73d76bb65caadd9092547578f7cb821e1c8bb50d90d5`  
		Last Modified: Tue, 03 Dec 2024 11:54:22 GMT  
		Size: 7.4 KB (7403 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a239a47dc8e5b6806865a5e03070765f807e7da9a0c102422dd3a07c529acd74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104072812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90eb7eda48c9009759efa5a71b21c19232dd9e939b9bfb8b227e2184996544a4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:c92b611280c7d224d58f2a2a7dfdc19380dda99a38e10495643ec0b43d2f3cac in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2039ab37391bfea5163cf2545fcb585344c981096040149e81aec9301f35f97b`  
		Last Modified: Wed, 20 Nov 2024 04:18:53 GMT  
		Size: 35.1 MB (35063190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335ed3d865eafcfc72459a536871a40009d4a399d947a0418657fd44f442c19d`  
		Last Modified: Tue, 03 Dec 2024 04:41:29 GMT  
		Size: 17.2 MB (17249971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19dd08a4345b11dbad4e6464f658a55387f7b1317148b558d997474d998e8fe5`  
		Last Modified: Tue, 03 Dec 2024 09:48:00 GMT  
		Size: 51.8 MB (51759651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c130a7e829a6b443f2b97c312dd323c9a462ca1e026e197aadc5b21ecc986790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5105613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1625028337b25c7ac210d33078ca5ac38f23bfd2e34520ad48f429c8ca92ef68`

```dockerfile
```

-	Layers:
	-	`sha256:a3c2a14b768bf44d6822d31a9593eaf47e27792f166ba4409c25ab3efc284940`  
		Last Modified: Tue, 03 Dec 2024 09:47:59 GMT  
		Size: 5.1 MB (5098257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86c20aa62daf40d0f747e05c4aa0d8c6812e31a7c227af22143256968b2ff99c`  
		Last Modified: Tue, 03 Dec 2024 09:47:58 GMT  
		Size: 7.4 KB (7356 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:433d7c7534db974f6efa271e3c5a0f5a505951ec05bc1521bdc947528b7810b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.3 MB (102294415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ca9a8119745c25aeca54ed77326269bf0a54ea4e69be1a42f0f6019dc22d93`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:76a233bff3b463f93cb832f44963527276c1cd491cd0a75c9c5d2eac75da2380 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9d51f6335bdd76dd9dcfd4d3eaa2272acccc262c17300716acd3ffb0ec5f5846`  
		Last Modified: Wed, 20 Nov 2024 04:19:07 GMT  
		Size: 31.8 MB (31787958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48e90448070e192152f471d2c8fd1cfc67ec60c6cb742a212ead9de030d94d6`  
		Last Modified: Tue, 03 Dec 2024 06:47:45 GMT  
		Size: 15.9 MB (15890462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4180e9749ee9c2cd33764d68a8a49f4513db415bcf81e499f6bd3b0b7312f056`  
		Last Modified: Tue, 03 Dec 2024 09:56:53 GMT  
		Size: 54.6 MB (54615995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:245d67b3be9b6d8a36b5477106bc596ada0fed35d74e3e1a31a6a15a7046e41c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5088461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd75e0600209041192ec38179e6dfae3df9f1dc2525c0c16567bc7347656842`

```dockerfile
```

-	Layers:
	-	`sha256:9d4e7dcb1858d2f2531abf6ef24471fb2839217b70f08b487c477e1dfd58b118`  
		Last Modified: Tue, 03 Dec 2024 09:56:46 GMT  
		Size: 5.1 MB (5081105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e42cb4187568748dbfad0592a9dae3060f3ea3d1ca9bd6b07064ed838f66c8e5`  
		Last Modified: Tue, 03 Dec 2024 09:56:45 GMT  
		Size: 7.4 KB (7356 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:6a9b27f24dfc6b4b5e36fc6f6151bb1580c136eb5a093d2d23f101392f7a30ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.5 MB (95486537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04161d746ba9ccae4b062c0456e0a82b55715a96f941ea113ee86cd4330059b5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:d8a0fd6e6a1b5571de35cb60b4e05523a0290523534ad63464fdf47dfbe0b041 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8ccad27fc3ed57037242d8c7dde5d5ce195749a63f65f7d9a663f7b822c4429a`  
		Last Modified: Wed, 20 Nov 2024 04:19:18 GMT  
		Size: 30.8 MB (30775034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d6a6da1657d09f717e7f94493d3e0563278583e47322d423316da636b93135`  
		Last Modified: Tue, 03 Dec 2024 04:11:01 GMT  
		Size: 16.9 MB (16937481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae51c456fa63fca49c43c89a34927e42baace55350a312e11092478ffa7894cf`  
		Last Modified: Tue, 03 Dec 2024 07:58:31 GMT  
		Size: 47.8 MB (47774022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:85a4c838344e21fdd6d0f53cf053cf9b033e8b5342d575dc09a6fc4a6355265a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5100212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690aa5a5d111b8e111274bdd5677c6c857f256dd71b29eaf8361700dd37e8047`

```dockerfile
```

-	Layers:
	-	`sha256:25b383443ef461e858ce8f8bd24de079c904448278eddb7473125e532a039dda`  
		Last Modified: Tue, 03 Dec 2024 07:58:29 GMT  
		Size: 5.1 MB (5092888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d29ee9c23c653e4f2f33a482a3aeb189af8c6d4b173b4ee25bd0046348f82cdb`  
		Last Modified: Tue, 03 Dec 2024 07:58:29 GMT  
		Size: 7.3 KB (7324 bytes)  
		MIME: application/vnd.in-toto+json
