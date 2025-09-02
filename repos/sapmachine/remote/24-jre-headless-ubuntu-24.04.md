## `sapmachine:24-jre-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:5792f66f761a19d74f36f21bee4dd2e59d5cc9d572df895dba4a385761aa8e64
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:24-jre-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:bc19e19cd2f5e2b9187ce4a554e19b8dd00d9a5581680fe73b8e59d0b45e4632
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 MB (96613817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219e9f00d42fce41280d8e8257fe21f61cc17c011fa708f8134ef1c5e0f4b092`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:20 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:20 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:20 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85479c0889a95e874aef7ebb1cf6532b8f9ed85a37f672e153211c2cc97adba`  
		Last Modified: Tue, 02 Sep 2025 00:24:58 GMT  
		Size: 66.9 MB (66890753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:435b6f4981536578ddf60f50fc890b3f9a97e907c6dc5c717f9173d32b722056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2292797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e62fabcaffe36df99d85d554dc827e17f2f573b46a82bdb2c7b8e47b8f4aca`

```dockerfile
```

-	Layers:
	-	`sha256:bd766205e5d96c014cdd2b31c3516431b05ffefce023cb9590c81b91416bbf70`  
		Last Modified: Tue, 02 Sep 2025 03:09:42 GMT  
		Size: 2.3 MB (2281196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c808bd3a6903c0327f678a99130364d76b0e38ccd6e4cae7c2ad8172ad320f4`  
		Last Modified: Tue, 02 Sep 2025 03:09:43 GMT  
		Size: 11.6 KB (11601 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jre-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:a41e94b667c08fdc6428b9e6fe5e9c3ffcd5126d4437b1db45a417eda115fe24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94797468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb2125d85c4c801c51e9a396667d06ae4d03f92e08d681c877d3e0066c7533a9`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:20 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:20 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:20 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab31f24a2bfb3d2441fd18bb3855651ae1f611f9a27b084a393727e451b6f24b`  
		Last Modified: Tue, 12 Aug 2025 21:14:48 GMT  
		Size: 65.9 MB (65937091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7246143bffe493059d528276b34214d3a03e39a33cee2162b26434316536193e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2293549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:608d54bb0c73febd4bf37990239a7b805dfda03017539ae18222151a48d5d44f`

```dockerfile
```

-	Layers:
	-	`sha256:65a0aadce0713a37fd2014adf84068676190425ce09f7bec4f1d394f2980e224`  
		Last Modified: Wed, 13 Aug 2025 00:09:33 GMT  
		Size: 2.3 MB (2281748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e9f47c4a16176f72990dd34da6b20ebb790266afa15f5afc744fbdbbe77adf2`  
		Last Modified: Wed, 13 Aug 2025 00:09:34 GMT  
		Size: 11.8 KB (11801 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jre-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:8319b829ad89646b0ffc4bbca96f7d093fb4246b9297ece546e386c8606a7c9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (101963338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb20d37c16a05b77cd95d4ee3f1ccb7bc85d9b696373b79ddc64ff8427bebcf4`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:20 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:20 GMT
ADD file:55e5af389c76b79c77275691d488810a1fd875fe7e47b4b14a8b70f1230bf1a2 in / 
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:20 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5128fb40eedc06172c4cc2920b45ddb874f5b42c161d0a777ed53f0b9f80b8e7`  
		Last Modified: Tue, 19 Aug 2025 19:17:46 GMT  
		Size: 34.3 MB (34329533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48149862eda7cf5716d342b7adb46e048c7c6828e961900161fe3eea19788bda`  
		Last Modified: Tue, 02 Sep 2025 01:53:15 GMT  
		Size: 67.6 MB (67633805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f796a96ee9ba7521f4277a540f6d318c7522a518ead08a632533ca7584f51a5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2290282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31526fbd79e7316912ee1abf11c969d16e86d936cb875b97688e376df6a40b52`

```dockerfile
```

-	Layers:
	-	`sha256:5ab593365f9fc1b79f4494e52391bbaee68b2368429278d35b8a134b08f9934c`  
		Last Modified: Tue, 02 Sep 2025 03:09:50 GMT  
		Size: 2.3 MB (2278590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da6f163375a1fa90bf8cd45fd3f467ce01092ee233bf45b2a1e706882cc53c54`  
		Last Modified: Tue, 02 Sep 2025 03:09:51 GMT  
		Size: 11.7 KB (11692 bytes)  
		MIME: application/vnd.in-toto+json
