## `sapmachine:11-jdk-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:f8b7a473607e20ce0fabf6ce46d4fa6463e3a5a7c271967cdf51efa93a32d9b2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jdk-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:d11c979d537269d483d5f7f821871f52cfba7edfd5886c6941a7be7f3b6ed208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227794702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:619598efe49213df8fafe1c6fe15d41d03a04da947028c4b785582064ce0f6f0`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68fc09aab137d82fd6a95fb40ae691fad4f76ca9b782352f305ba0dc0fbe5ef`  
		Last Modified: Sat, 17 Aug 2024 02:02:40 GMT  
		Size: 200.3 MB (200282933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d25875372e160027bfaa3e58e613dff82574d6fc093fd7d43795139833a9240a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2391815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd1f4c047cbed3d3c20e6a0eadb7715a6d06a4a15bd2504c77f49632bbe91ed3`

```dockerfile
```

-	Layers:
	-	`sha256:421be81cd2b046b0ca06d7ad050274cd1e312330c5b55d38c12a247820773ccb`  
		Last Modified: Sat, 17 Aug 2024 02:02:37 GMT  
		Size: 2.4 MB (2381931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96662f8f5f1ee19c42e9278aea90a6212de90babf879d7116de68f95513c8b95`  
		Last Modified: Sat, 17 Aug 2024 02:02:37 GMT  
		Size: 9.9 KB (9884 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:4e225ceee97e5e430d461fb35d35095bebe2e8af71185dc65d655e4289b9331f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.7 MB (224742705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74bb2cc9715ac10ad01bbfa9f0556bd1bb98a0913f9562d756550d068d172eb0`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf39a23381ea0ac7f09773e26049a38726ce382223fceef5875b06e5e092ffab`  
		Last Modified: Sat, 17 Aug 2024 04:49:26 GMT  
		Size: 198.8 MB (198768488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5bfad6f7a216f233a12b7da9ed84caa447b8c2dbe59f57de90a031793fb2af72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2392476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fedc76fb05d217cfc3a827c2095ffb6ad452938898178bd5daaf9331119f1590`

```dockerfile
```

-	Layers:
	-	`sha256:e13bca14ee514c37a19cddb81eab57233ec9f3d4debe0676604e2cda7f931d24`  
		Last Modified: Sat, 17 Aug 2024 04:49:22 GMT  
		Size: 2.4 MB (2382243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d38672cd200fd612c3fb47d6026a0f2ed922f9713fad37bba94b15ccc5948f1`  
		Last Modified: Sat, 17 Aug 2024 04:49:21 GMT  
		Size: 10.2 KB (10233 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:42df88be4ff22dbf639f890417392e45b67ed9377bdac38a09975aa422a073b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.6 MB (218625984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c92e636ed8de3177758109f9b248ea461ca212a2fd94b5cb8ebae552c51ce9b`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f3b175423e2add884b475baca08015a389b9791d811b3b5578a0b60aeb7e2923`  
		Last Modified: Mon, 03 Jun 2024 17:20:01 GMT  
		Size: 32.1 MB (32077140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1e338333a2e717e5fbac1cc8b3988c3d4e80e9e0b8729fc0f61a598f9a68ac`  
		Last Modified: Sat, 17 Aug 2024 03:40:23 GMT  
		Size: 186.5 MB (186548844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b691beb91083cb260da4a98935408cb4be1d233ca00ca0540312b6a4d5ddcadb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2393092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55494de2dbc55a7e71edd43ee2e73fefd911d714acb2a96947baa76263ca3182`

```dockerfile
```

-	Layers:
	-	`sha256:e89d6306927520a08686740c2eb6943ac72fb5ad31db08eb1f101800aafc7f48`  
		Last Modified: Sat, 17 Aug 2024 03:40:18 GMT  
		Size: 2.4 MB (2383146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:580eeba762873769e3080d0a833d5325b69b5baf1110a69066a930313ed8f148`  
		Last Modified: Sat, 17 Aug 2024 03:40:17 GMT  
		Size: 9.9 KB (9946 bytes)  
		MIME: application/vnd.in-toto+json
