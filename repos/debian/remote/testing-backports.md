## `debian:testing-backports`

```console
$ docker pull debian@sha256:1ff53efb8da1730d9cb473f8de7d7bd766182b3c63b5dd0747ff83e54403dd29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
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

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:c94a3c5afc419d95b9d1ef59eb988f84a6eb9aff7be85f5e0acd94e0636a5cf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49737039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0406cad4ded4d7a6a8a1595d3fc0e558a416ae0992ddc4eaf7b563c46c8b5443`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e53bf7ab07ea4ef0bdd293b1b3d03f786cf07ef52cf9fa96c661bdb1e7e3d20a`  
		Last Modified: Mon, 29 Sep 2025 23:36:06 GMT  
		Size: 49.7 MB (49736817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:265f039e912e15dd81fca61ad79edd7d56dbe230493bbca2421904544a323582`  
		Last Modified: Mon, 29 Sep 2025 23:47:28 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b938feaa474f9f30bd2581056424eb9684bff957f84c5d424296fe2d4b9b0d08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3170483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc5b3ab8305b848cfbb624710fdebb6ab7d4d7c8667095946ae1c26964ad39ce`

```dockerfile
```

-	Layers:
	-	`sha256:a90ffb1cc0f85fe9c2a439e0d555f71109a2be555164f945e5f8983e0e2ce95d`  
		Last Modified: Tue, 30 Sep 2025 00:31:25 GMT  
		Size: 3.2 MB (3164646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39aedcc3bbda1ea198abb54ddf537b5d810c1982e2c0c162d7f2f0916c3590ca`  
		Last Modified: Tue, 30 Sep 2025 00:31:25 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:c45b46888b545c120ca511747c51d8e9acbd613d8dfebf3f93576e7ad14304f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46021065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84140c9615b1ea2fe9cd4aed42c8932096de0171aecf4bf2ac5fd7496a8d6a05`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'testing' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e0c42b30794d7809e756b71306a8a347b4104aaff80f2934d3aba31ef14da533`  
		Last Modified: Mon, 29 Sep 2025 23:35:24 GMT  
		Size: 46.0 MB (46020846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c340acf86cb58beaaaa762ba2cbd4d5000a4c4b2b785cd2200bc722233dd167b`  
		Last Modified: Mon, 29 Sep 2025 23:53:12 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:2aedec6f1614464b8f9b35635dd2fdb0801d8c629c077df1a4889e7ced0cd7e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3171913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:817bc999ddb2943b41019c0a304db7969e4035674470c7d93bc8eae33ecae053`

```dockerfile
```

-	Layers:
	-	`sha256:67365e5f222bee02e52637fdfba5724f89bdad41dfc8d66f662c21aa10728ab5`  
		Last Modified: Tue, 30 Sep 2025 00:31:30 GMT  
		Size: 3.2 MB (3166020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13e6d7158d47d70e5a05c948ca8c3366371aad45fe1638de274366a3afa5e7a4`  
		Last Modified: Tue, 30 Sep 2025 00:31:31 GMT  
		Size: 5.9 KB (5893 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:fdbf760c3f4935382d6c8e266e7474dcba6d1d8fd0c3c4335ab25a3df002b3a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49880098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05d2cb47d240dd8bda0f882fd00bcb98098200bb0a3355e7d508dcdedb27b6ed`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:eaa39e59530b026aca4c6a2bd8547ebc0f3668ab204470b61baf267315ca1cf9`  
		Last Modified: Mon, 29 Sep 2025 23:35:15 GMT  
		Size: 49.9 MB (49879876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99bb4f73d6fbcb317c728eaf73faa8101823b98c01852ba3b21dc3cd285c10e`  
		Last Modified: Mon, 29 Sep 2025 23:48:05 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d3262c6baefcded1d9d4a569c986bab4319396a01b486ea398f5320a98f95521
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3172032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c763c07ffff08bb8926c4679b22a8158b938d22b4e810ccaea8934a03d7ae78`

```dockerfile
```

-	Layers:
	-	`sha256:ae63969eef83da765c8e8d3c852d8c1ef3777472f433fee35d423a6099476f9a`  
		Last Modified: Tue, 30 Sep 2025 00:31:36 GMT  
		Size: 3.2 MB (3166127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6568dddf56c31880fc502a51beaaeba927eb19ff40c373bf283c49398826ae4`  
		Last Modified: Tue, 30 Sep 2025 00:31:37 GMT  
		Size: 5.9 KB (5905 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:500a91968cb66cc888b41b324c4f2a659bd7502e63f7bbc8110f07c8cf109a59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51119640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bba379353c8d471e217c27d464d84d65a4f16989f41abe802f8f61b0924b036`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'testing' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e4f313a379a9bffd32c298c8af86f7e155ff0aea7519eee23a8d28bf9b6fcbfb`  
		Last Modified: Mon, 29 Sep 2025 23:35:30 GMT  
		Size: 51.1 MB (51119419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc84173b4a9033dc25e64c0589ccca398091d4ad6ae807e2cd72cc38e5745b9`  
		Last Modified: Mon, 29 Sep 2025 23:55:53 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:69ae4d4ed32f9c1b516969787c70bbb80d097e1a30d93abc664a6b6347cf9da9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3167670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53e85f809546dea620ac89ffae72ac34186b5f9540196431148da41aab3c192c`

```dockerfile
```

-	Layers:
	-	`sha256:c2dec28c6b0475ee3cbc06d24e781944b56c68fe352f8dc3b2fa929e60acd97a`  
		Last Modified: Tue, 30 Sep 2025 00:31:41 GMT  
		Size: 3.2 MB (3161851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:464fd10f0e7f24c8148f1cd12d3e4175f26227e9b278577f58fcac3d9e026385`  
		Last Modified: Tue, 30 Sep 2025 00:31:42 GMT  
		Size: 5.8 KB (5819 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:81a8988bef958b1c0bbc3fc519c847d391ea50a3b7db60651d6e394971ed82a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.8 MB (54751100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe973959263979a534685df9f8dad4bb558805e5118312806eb9dd022909201e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:62b863443040ce1d4ba90e93d398f94c1ec68f34663867e17f1e7b87f9d7dc79`  
		Last Modified: Mon, 29 Sep 2025 23:40:28 GMT  
		Size: 54.8 MB (54750878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e7cc95aa5333d7909cba4b6636cd9b90542ec4736f3fa4f094bd677b1fd3d0`  
		Last Modified: Mon, 29 Sep 2025 23:51:05 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:4f3f7863fcf4c13f6ff29e60c4d6185cbd79db1a815633bb6c7ae5d2a2f8d626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3174016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4582e68be5d8d62db1eade394a246b95df417bda231dcb97c5bf50d2a52249`

```dockerfile
```

-	Layers:
	-	`sha256:6de63765c0170e0b1700dd817008abd1f8346313d39c8cf379f22bed468d7cdf`  
		Last Modified: Tue, 30 Sep 2025 00:31:46 GMT  
		Size: 3.2 MB (3168153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d3e03a58890910e2516a3aaafff64216cb9ab0e44f303ee9b042685340ea387`  
		Last Modified: Tue, 30 Sep 2025 00:31:47 GMT  
		Size: 5.9 KB (5863 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; riscv64

```console
$ docker pull debian@sha256:5441ab7e6a37438f40f5016ff55968086fa7929b4929511f64777d38be1430ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47970316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c764081f9a00e28ddd8126387fc37e949fa9e7c55e4975c0fbc33fbed9bb4df7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'testing' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:0f1822446ca45f33b7c453fe4bcd50fcd0ba47d1e327657e8d1efa0c719bdc40`  
		Last Modified: Tue, 30 Sep 2025 07:09:06 GMT  
		Size: 48.0 MB (47970092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e4ab0dfe07e01ec22bbf1da1ab7ae8b7730436ba83847be4cae7c6cf623274`  
		Last Modified: Tue, 30 Sep 2025 01:30:26 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:f6fc3d5d9d3e74cf8a22206eaf13abebec5d5d2be89d5f365f3d1efa8dfef64a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3162818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cdd00c8f72d1d821b72271eb343ea6798f68921080395c53bf794c168c1af22`

```dockerfile
```

-	Layers:
	-	`sha256:1468caf6d7b21d4898c207c5f253c82e7aff3e2c1b3469dbe1779e5300e3527a`  
		Last Modified: Tue, 30 Sep 2025 06:34:45 GMT  
		Size: 3.2 MB (3156955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60187d08cf65c01b89054ff3dfc345e5aaa7d3f4c1235c3d8d19649559a0710a`  
		Last Modified: Tue, 30 Sep 2025 06:34:46 GMT  
		Size: 5.9 KB (5863 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:1b3bd5143df140264011a4ac2bb0c30406ec006dda29eb3c187c1b78bced0a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49576233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:089fa00616eb5940d73201e2c0b4c9dc6a9c416d697a495aae69ab77ded9d5c4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:6a0a4867ef73eaafaa3876eab73c35b9c7a731cb8449516b6e6ca5e9b88df7e9`  
		Last Modified: Mon, 29 Sep 2025 23:40:06 GMT  
		Size: 49.6 MB (49576013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d98a8623c07812daf2248fac38c8c2c1d3a0900fe2a2c88b554a41a45f965e`  
		Last Modified: Mon, 29 Sep 2025 23:48:13 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:df105b8b15d9b1c1eceed7577169050ad2e2f052e46ad89045a8aaaf4c76e784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3171930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b1fbe3d2a11d75b010d90c9953d4fd4e5f17582113d175a5441d386d4c0271`

```dockerfile
```

-	Layers:
	-	`sha256:c9e25d82b07da11e8fb7f6a6a0d5f0bf24cb763d3daead9c40b03f0dd06c1610`  
		Last Modified: Tue, 30 Sep 2025 00:31:55 GMT  
		Size: 3.2 MB (3166093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c14fd7ecdbd986ed4f5dc3a86598589fcc989561fbf7e5ec1201576a2d6bb96f`  
		Last Modified: Tue, 30 Sep 2025 00:31:56 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.in-toto+json
