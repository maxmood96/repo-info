## `sapmachine:24-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:5eccd3eec2eab504e51a3eb97ee85a4b655e008e4192590a49c6e272c26b0105
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:24-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:e230fbcabc056b778a1451a717bc3d998fdab85d11ec0eab27feeb0dccf83ad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.1 MB (259072540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4c99ded0445676080234be8a304746bd9ed6f2a8ecfc8a66e08b66ed5d196fb`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 19 Mar 2025 14:31:37 GMT
ARG RELEASE
# Wed, 19 Mar 2025 14:31:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 19 Mar 2025 14:31:37 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b14b84e538a124d71a956b0c4927ef62171d1be199b6d94384deecf55fa9c0d6`  
		Last Modified: Wed, 09 Apr 2025 01:21:08 GMT  
		Size: 231.6 MB (231562146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:96435d760de4407c855636d9c5a001b431f730f41ad0fa121f99dffa9dcaa635
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d04356a79bdd0418f3f94f2bbb1352fdf81d36e2c63f27176682d744e13458fb`

```dockerfile
```

-	Layers:
	-	`sha256:dbd95bb1f879038a711cc0f94cca39a1678840cc0cb16add9e6534c58ab56bfd`  
		Last Modified: Wed, 09 Apr 2025 01:21:01 GMT  
		Size: 2.4 MB (2376040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c75753289dbee3a138366cb4e42a49326a58091c45fb9ba73f9432482154278`  
		Last Modified: Wed, 09 Apr 2025 01:21:00 GMT  
		Size: 10.1 KB (10058 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:9ec1d8bfc99365016f559e58ffce8f426e2bc04233ea3a9ab122c73c191fde28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.5 MB (255455974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a7f50c830b37491f84d0bf5e0eb6a1095224849899590d86087b4c1bd9bddaf`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 19 Mar 2025 14:31:37 GMT
ARG RELEASE
# Wed, 19 Mar 2025 14:31:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 19 Mar 2025 14:31:37 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d680311638e0a0069b9e3ff661bf365d484a4685462de19335f7c9cd5195716e`  
		Last Modified: Wed, 09 Apr 2025 09:25:30 GMT  
		Size: 229.5 MB (229478313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:76ff8ba2fb76705a1f92cc6d8c432a5682a80e454fc1bea83e362a7919a49c61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d320b011ebb16af6bbc08387d55da47ac2cdade3481a9763e4611f437e3d2108`

```dockerfile
```

-	Layers:
	-	`sha256:86b71754c118de42fee24840b690dc5e191539e00167d256ff386587767269a5`  
		Last Modified: Wed, 09 Apr 2025 09:25:23 GMT  
		Size: 2.4 MB (2375723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a92319d04c727d5c8cf5ee91a0ea0cf763ed505dccadf8497c26df1b8ef4e7e4`  
		Last Modified: Wed, 09 Apr 2025 09:25:23 GMT  
		Size: 10.2 KB (10213 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:324d77a93bb36e88574deacfb4ecdf9d06e8d16f77b23f3d038f77934202dbb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.5 MB (264486614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c74d618b490107465b95d4907402f7af6edfc3c5c7b833d873ad724c7c9b0f52`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 19 Mar 2025 14:31:37 GMT
ARG RELEASE
# Wed, 19 Mar 2025 14:31:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 19 Mar 2025 14:31:37 GMT
ADD file:d85970cec61787609e3854cb76ce16d54fe420b254cf48fc9ed9ed678717ff28 in / 
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:92d54367a68b4f03400315732acb4290d88bb06f8fe1414fd823f93402bec922`  
		Last Modified: Tue, 08 Apr 2025 11:48:44 GMT  
		Size: 32.1 MB (32076946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:804a37a916fbe5176c5709de709c22223e6c5072b075e7f7517fae4796ec522d`  
		Last Modified: Wed, 09 Apr 2025 06:45:18 GMT  
		Size: 232.4 MB (232409668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5decd2549328ee94a555164070b58671e09a26bf838090b1bc14ce094317b7c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2387396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:124de9ab58c41151605215aaacd94309374098e26e6e8ba61a362421c1c840f2`

```dockerfile
```

-	Layers:
	-	`sha256:cb19ecbe99f5c5c6419515f852eae6b1333cdc0d37c77681f672090deb9085b3`  
		Last Modified: Wed, 09 Apr 2025 06:45:12 GMT  
		Size: 2.4 MB (2377267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f67ebb347df2732287e03f0bf08a86eb7016d204b7e5ac85155a90c28e68b05`  
		Last Modified: Wed, 09 Apr 2025 06:45:12 GMT  
		Size: 10.1 KB (10129 bytes)  
		MIME: application/vnd.in-toto+json
