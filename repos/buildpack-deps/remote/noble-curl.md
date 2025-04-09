## `buildpack-deps:noble-curl`

```console
$ docker pull buildpack-deps@sha256:130fe02e4ba5e3b75a59e13385d0712f2debc246348ba27ecc10fcf3b2a92356
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

### `buildpack-deps:noble-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:a48cdaa2e08ef61b326ba11ae2260a17e40861ceaee8ffaff7bdaf3886ff2a23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.3 MB (43337869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56f10cfd590b968a5b89adcd76c573b8fcf847aa106f627f661734f8e1514eb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69309ca3d9d60664f532872b9e1059b60a35b8bcd9da011efbec14de1397debb`  
		Last Modified: Wed, 09 Apr 2025 01:11:36 GMT  
		Size: 13.6 MB (13620217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:29cc2d4b0730bc00b79d390ec85c53409956a8ab5edc7d487fd5a295579c9990
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e280959de80767bbca83f5e4d0203848ad53d1682f1d6e2e238e4635d1fcc990`

```dockerfile
```

-	Layers:
	-	`sha256:2434904d4cd7b78198c720f9fea8e5248eda28c076698e9ed58c2a31dcbd7eac`  
		Last Modified: Wed, 09 Apr 2025 01:11:36 GMT  
		Size: 2.5 MB (2460509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:458bc3c7e2f546b5320ff7f605bce714acf3561711e3b3f94a56b753f9b03c1a`  
		Last Modified: Wed, 09 Apr 2025 01:11:36 GMT  
		Size: 7.0 KB (6959 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5ae44b9cc101087fa183a9f8269d6d8f0d1c86230044d58ec0015e1fa706e1d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39645632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19c0792edbcf8119e6ef8d42938209118401d44f50d9674972ff99beec67a6aa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:22301ffa2fa465db7a0f07e0c3ddc488f07cc6a745c39e6f450fdbe37da97418 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3492abb11babfb77cfc5a8904e67b22f4e4fd68c8d8a7fe1119861ed6503b36f`  
		Last Modified: Mon, 27 Jan 2025 05:10:02 GMT  
		Size: 26.9 MB (26874983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d26a8223ab81b7619d0fa204eaa4a52bd9e82a52dc44e8e3fd181d828b57c69`  
		Last Modified: Tue, 04 Feb 2025 10:45:28 GMT  
		Size: 12.8 MB (12770649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:88d98aa301ddf4ba195ae435b272e8dbc57ada124bc050d9584e020a2d0ed4cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2471405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f632e6a7a1f74c013a8732986b2644111dec9298d7588b4e37b61e3e5f87211`

```dockerfile
```

-	Layers:
	-	`sha256:e39ed50c31a6f47c59f9ff236393152bf088df00a815272e7d5f17eb16b93ed5`  
		Last Modified: Tue, 04 Feb 2025 10:45:28 GMT  
		Size: 2.5 MB (2464386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0299afeb76c3ef583558026c326712b4428d9f8d2f847835de29e219d670197a`  
		Last Modified: Tue, 04 Feb 2025 10:45:27 GMT  
		Size: 7.0 KB (7019 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e6b609344ec9798eed5b74d3afaec418c234088acecde00481e2938174b2382c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42302345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f38f397b299f5adac2d13c33fd3f4c8875aa79d5c3d4cc56a1052d9f7dafb649`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174dd04251589e381fa1e70743cfe3191b94d8402a613012606a57ed34a68108`  
		Last Modified: Wed, 09 Apr 2025 06:10:17 GMT  
		Size: 13.5 MB (13455387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:18d1de137fbd14ef9e12e53ef0d75e9640c96e648bec45c2979f7fcd0c0861e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad8cca304df6c6e8d56adae4eb4cc4e4246cd9d89c7fcbdea1ea4a395867798a`

```dockerfile
```

-	Layers:
	-	`sha256:ba7ae120372fb638b2725b7e354561a90b87d8f9c43bea7235bbcfaef98fe0ac`  
		Last Modified: Wed, 09 Apr 2025 06:10:17 GMT  
		Size: 2.5 MB (2461567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1866b27b704c6b875efa7f9b3f6e691a980ed8df014a15ce2f307bae67a39b6c`  
		Last Modified: Wed, 09 Apr 2025 06:10:17 GMT  
		Size: 7.0 KB (7039 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:0b1cdc827579f6d923954e24df1568890141b024b25f938096272b56fd8f5feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50292632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dfa9b64e1a14e17bccddbbe1efd4ad8103936b9d0a5b6ceac71db5b8e96c9e8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:d7a12d3d510b1bacf894dbb7d42f36de9391b0766c28643a60d20d3c37a12762 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7be894b3e11d60e6c310a10016f7c569f1a313b370ab3964114b1c135b1ce53c`  
		Last Modified: Tue, 08 Apr 2025 11:53:59 GMT  
		Size: 34.3 MB (34340867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f1c8bb3d99b4917c8ba06f9646b55d42ffc7d868b7d8010468bba3dabffc300`  
		Last Modified: Wed, 09 Apr 2025 04:29:36 GMT  
		Size: 16.0 MB (15951765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3624eea40880c7c06f6e5021d5fd0d68ef5e73117ef4755668f124b415e6d12f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2471987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b884180b00a0e58e77109971199061b3014cf28092a343ca03eca18b4649c33`

```dockerfile
```

-	Layers:
	-	`sha256:18dfa50e0eaa2222a04cb6fbaa9500965e9c1ac41252388db5608ffc35f33f24`  
		Last Modified: Wed, 09 Apr 2025 04:29:35 GMT  
		Size: 2.5 MB (2464996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbbc7bdf9f121280f0ac7d7a92189ef2b9747aeb6f07ba38982b3cd324d0a067`  
		Last Modified: Wed, 09 Apr 2025 04:29:35 GMT  
		Size: 7.0 KB (6991 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:6b02b22abee9de25f956428231a61881bd8e4a7759f00b476c72b31cca4e9993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45270563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd737fdd04864a275174d5fe0d7967fddd7ff0a69b3a3c38dadb832d477c5b82`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:ef7c97f5dd8d665aae899afe52c54f7acaf71fa51e9d7f26e13ed6073141c666 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ba2f284f7444fb0b78fa804d74c44dee4b397610267539e4a6e9c41ae41e06a1`  
		Last Modified: Tue, 08 Apr 2025 11:54:06 GMT  
		Size: 30.9 MB (30943202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5f313a1c6dbd13467e879d320aa46ad9e7a8abb607e47f5fcd4fe19d104810`  
		Last Modified: Wed, 09 Apr 2025 05:18:21 GMT  
		Size: 14.3 MB (14327361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bdbcbb02850b253fa51907665a357cb34bafefa687080bb7ff0fcf31507da682
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2461559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba84c05032e7a50720f80859ba0e2b1ff954dc7e03599461f668bfc8fbe89287`

```dockerfile
```

-	Layers:
	-	`sha256:92ddc09fbd07afa5a520aa26aa20911f536c490ff5f2fb76ef5849884c54fe7d`  
		Last Modified: Wed, 09 Apr 2025 05:18:19 GMT  
		Size: 2.5 MB (2454568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51cc1d4cd74da79a256fd69e7e8f7484f7c5bc4f63d0bb2defc509310b75f9de`  
		Last Modified: Wed, 09 Apr 2025 05:18:19 GMT  
		Size: 7.0 KB (6991 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c66d1311cc359c238584546240798860d0054e0afd83a5b42e8a810772edab3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44893717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0173b2740d5ea9e0ee934f26cd6713ea3fc8e47f178d790d47328d4d635e3a2d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:8f287f40ca940c9bd87c8706751f5f1c5bbd0a83fd75f7d938832b226fdb936d in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e5722f32c6281fa87f1e5f7ebe307864b50aa95a116496a205ce47478bc9b52c`  
		Last Modified: Tue, 08 Apr 2025 11:54:12 GMT  
		Size: 30.0 MB (29956206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e704885473e9016559440f7dd673fed8248fa9c173ce47190caab5bc5ba71e91`  
		Last Modified: Wed, 09 Apr 2025 04:12:34 GMT  
		Size: 14.9 MB (14937511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2e3ce6289d6dfdae13bdc6007e7827753610faf61af09b03b72d486ca109db99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2470293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe9b44db1e2b4b7023779226728773fd6e76c034f80a3c6cdd82786b9872b8f`

```dockerfile
```

-	Layers:
	-	`sha256:4368cfca770fa4fdb1411663342c39e4df496967e45af14cffdc07010d681b3f`  
		Last Modified: Wed, 09 Apr 2025 04:12:35 GMT  
		Size: 2.5 MB (2463334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:463a7155304f33a6888831fd0036b81f064c133ac2211b8de31b8fadd0771747`  
		Last Modified: Wed, 09 Apr 2025 04:12:34 GMT  
		Size: 7.0 KB (6959 bytes)  
		MIME: application/vnd.in-toto+json
