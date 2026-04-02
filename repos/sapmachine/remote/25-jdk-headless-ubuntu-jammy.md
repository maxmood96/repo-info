## `sapmachine:25-jdk-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:ad343bbdfa62c5d31a79d9ac3f7c33da02d5ad8e08d26f7318dc2213c43997a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:25-jdk-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:4cf11a070afe519223e155e9297669affbd7f1078019c4d0dcd62eabb1902c35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.6 MB (249591510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a642d5d3ad54cbecd142ca32c0760ce91e69d53f89e69b1f0ad7ac9650e76fc7`
-	Default Command: `["jshell"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:16:01 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:16:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 01 Apr 2026 20:16:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca042fc8ba1805eccd895afe70c337ec782c44d32c746751e8f081aa1f2a644`  
		Last Modified: Wed, 01 Apr 2026 20:16:25 GMT  
		Size: 219.9 MB (219855097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:129871a99c29beb2906746429175696a7d3c46fd4cbc7b6da3d21d20b9cfa674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2379778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:135b0b8445993069bd211664261c58dadfa7a5c31b21737a0172b2103c8c31f3`

```dockerfile
```

-	Layers:
	-	`sha256:91d52b25de42b275c278c5ba85a4b34ea087a3b68f4f082ac09765572a320371`  
		Last Modified: Wed, 01 Apr 2026 20:16:19 GMT  
		Size: 2.4 MB (2370194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e36cbc2f4afabbc21b55026bce2be773a003ac4e972f6016eb8fa35e86c6922b`  
		Last Modified: Wed, 01 Apr 2026 20:16:19 GMT  
		Size: 9.6 KB (9584 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jdk-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:f43004041d2ed339c1229d0f4093ee59685db4dd37012341a642cb62b45bfa2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.2 MB (245225555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:697d32c44c4248a848fea5be7136fa0e62821ed3970691f7625b68e96d284f46`
-	Default Command: `["jshell"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:15:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 01 Apr 2026 20:15:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a725e112bad2d0c168a2711abae194a826ec7025fe98baafb9e6b7bbb99fda67`  
		Last Modified: Wed, 01 Apr 2026 20:16:05 GMT  
		Size: 217.6 MB (217618612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6a9eb0f2fdfe6a20a79136595c5a764e8da6e340227e34a307ba5685052adce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2379600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d87590f4bce57deef14ff393e0f3f67d114919b4ea38628b2937e5221bf58c0c`

```dockerfile
```

-	Layers:
	-	`sha256:8d95ece825405aea4f8e7a533e223b969d9f1b7233567b377d81271afc249193`  
		Last Modified: Wed, 01 Apr 2026 20:15:56 GMT  
		Size: 2.4 MB (2369887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6308a50ee3e0ca82da6e37363483e51c7a3d19cbd0de107d39db6411cd264cc8`  
		Last Modified: Wed, 01 Apr 2026 20:15:56 GMT  
		Size: 9.7 KB (9713 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jdk-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:3e8eb3277cda38c8c307a621adb827ce7d674062ae775e344b25f13419a3cc85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.1 MB (255125444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:319f299ac118019f83097ba01c16dfed2438725c3a44411a031fb1da482400fb`
-	Default Command: `["jshell"]`

```dockerfile
# Sun, 22 Mar 2026 18:11:34 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:11:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:11:34 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:11:37 GMT
ADD file:268be611d24f69c3d8e480314cd587652e4c89a6032236737057c8b64f2379da in / 
# Sun, 22 Mar 2026 18:11:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:45:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:45:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 01 Apr 2026 20:45:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6fb1b04a0a70d070de8a04181c7b855a46b1ea4f771660ae7f0783acd4569be2`  
		Last Modified: Sun, 22 Mar 2026 18:43:46 GMT  
		Size: 34.6 MB (34649660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626871d74fba87a0b9c1806031b3cc5ac58fea17a733935a3733aab9b3b61ab8`  
		Last Modified: Wed, 01 Apr 2026 20:45:58 GMT  
		Size: 220.5 MB (220475784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:294c37ec9bed383c98f211d0fc02571baef9c3d6ef3ce5dd79999896c2238e73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2376725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:791e411e4c3659b24c555f821b150fcfb797484949d4d01fdab00cf2bb9ea0e1`

```dockerfile
```

-	Layers:
	-	`sha256:52b782ebae149fc98985c0e51001756ba7324186ee1ae897594eaca5ce7ad875`  
		Last Modified: Wed, 01 Apr 2026 20:45:53 GMT  
		Size: 2.4 MB (2367084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98974b543df7dd71ff1e826ccf9191feec87c5876e72569e8ad1119e71b7e578`  
		Last Modified: Wed, 01 Apr 2026 20:45:53 GMT  
		Size: 9.6 KB (9641 bytes)  
		MIME: application/vnd.in-toto+json
