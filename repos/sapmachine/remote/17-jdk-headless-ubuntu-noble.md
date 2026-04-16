## `sapmachine:17-jdk-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:720d8ba9e41edae4c103a6b0bce0ae761fc9d1f6781007b93e77dd1b1572181b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:59cf6020e38a312b9d4054c54b26343e2bf43eaee60c5d21015d8c673ea6ad89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230244936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:084efff0b64d701cdeedd65587eaebdf3696d7c1786f22309fc2eac645ab68b9`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:59:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:59:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 15 Apr 2026 20:59:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb40b2922ee7907d2711a2ac733078a297fdfa51d288a6cb9e79f0d58ddd6dd`  
		Last Modified: Wed, 15 Apr 2026 21:00:18 GMT  
		Size: 200.5 MB (200511958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6bb059fb5ebfa9ce44c1fe8970e322721ebe6d64f55a502b47d8f60d7e11e81f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2367122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b7994b8283ddb5beb1930248786d8a94e017e60f787d5347ca2bddadce58509`

```dockerfile
```

-	Layers:
	-	`sha256:5d7f7113a17762bfbfa968c70ec7de3b81ed5bc217e23c347788a2158a1230cc`  
		Last Modified: Wed, 15 Apr 2026 21:00:12 GMT  
		Size: 2.4 MB (2356888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48ed3f9efbe82b1a576c491c210d67fa593abaf254769ac73402434888a5809e`  
		Last Modified: Wed, 15 Apr 2026 21:00:12 GMT  
		Size: 10.2 KB (10234 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:61f2a1d2dea6f03e2878fa14069780c42f49401a8ee8dfbd87d10434071a22d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.1 MB (228103206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e2d5a793fd2b605ef583da08a7b4d7f3a0236418ba490a8b16424a4d673703b`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:10:18 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:10:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 15 Apr 2026 21:10:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa121f4831af8c06d3a19758d9c5f97f135d22710c3a3e8b91b99f35bbcf331`  
		Last Modified: Wed, 15 Apr 2026 21:10:42 GMT  
		Size: 199.2 MB (199227421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:fb774f9bb24d90914f71ca2367a3eb387705385ad9bdab47a6653369da9035e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2367781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73a4215932404a64c35328887acc9c45060f97ceab1bab55074d96e8d15a591e`

```dockerfile
```

-	Layers:
	-	`sha256:7302eff7ad2b637c41cdc86c187457f21e29ab387a2df739058e26041f78d662`  
		Last Modified: Wed, 15 Apr 2026 21:10:37 GMT  
		Size: 2.4 MB (2357395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bc2d692e9980035eed63ae04f16e57eeadd2b8c1501b8052f0681a60080a85a`  
		Last Modified: Wed, 15 Apr 2026 21:10:37 GMT  
		Size: 10.4 KB (10386 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:e629adb4a9214280c31e2c431f46ed96eb384dcf31561d356b7443476e389837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.5 MB (235490810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a4f24d555a439e7a25dc630a61c4cc4da922d0e8e0417569236ec5402554d31`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:25 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:26 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:29 GMT
ADD file:ede7e3b047d459e8abfd20afae677192c0eab70c709496e87b2110289bfb5f3c in / 
# Fri, 03 Apr 2026 15:15:29 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 09:11:30 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 09:11:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 07 Apr 2026 09:11:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2206a81f65df3147f8c62d4c01c47495515dae16f93ce6845cd7cdacdd206f1e`  
		Last Modified: Fri, 03 Apr 2026 15:56:51 GMT  
		Size: 34.3 MB (34313334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b5615cc34c37269d7066e166fcf834f966ab128cf40fc521c3ac50a24653377`  
		Last Modified: Tue, 07 Apr 2026 09:12:17 GMT  
		Size: 201.2 MB (201177476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:444b30306214623d1081d11b9bcdcc02b143bc23520a50baff57301bd914e8f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2364661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f708aea2ff6b40de2271d8dc000a411d4f21f2a48f414782fb3e7e4d19d2b409`

```dockerfile
```

-	Layers:
	-	`sha256:91b4b1fcad1368e74c0e1e837e98b41c766a76a06eefc15309e15ba07a6dd5e8`  
		Last Modified: Tue, 07 Apr 2026 09:12:13 GMT  
		Size: 2.4 MB (2354359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4fa8c0927ac000338a29a42d801d9209143aab3c3698f111efe0acec070d0a0`  
		Last Modified: Tue, 07 Apr 2026 09:12:12 GMT  
		Size: 10.3 KB (10302 bytes)  
		MIME: application/vnd.in-toto+json
