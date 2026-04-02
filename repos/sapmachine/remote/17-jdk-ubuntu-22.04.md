## `sapmachine:17-jdk-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:593a1005d2edea86b759a28e40748104ba692739d78604795b6e8c182cdba7d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:d656aed2a2b7bf11c9a77df499d877836fa02d6bf5e8780636650b688c2e8a02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (231034805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25c7f3fdb929be5d4948312117e66339d0b5d526ab346e8c70bb39359cd75f9a`
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
# Wed, 01 Apr 2026 20:17:08 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:17:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 01 Apr 2026 20:17:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197ae8e77b740b44fe6c13029d06987c26dfc6e78938d37d3a990389192a9b28`  
		Last Modified: Wed, 01 Apr 2026 20:17:31 GMT  
		Size: 201.3 MB (201298392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:48c05095d945ef735f51958d6ed9bba1c1380493305d84b2067f3df561b713ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2640346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:448c5e3bd3caf7c216901a547864664e59f05848be8ecc8644fea6933d659381`

```dockerfile
```

-	Layers:
	-	`sha256:2f9314947504b84a349315c35028c33d6a45bf4f6e2d4bc4b8587a5514aedd9c`  
		Last Modified: Wed, 01 Apr 2026 20:17:26 GMT  
		Size: 2.6 MB (2630251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:926fd34ee00214149550a22a4ea0e7bd71c5fb8d1e992e1032c397fe50d3ca46`  
		Last Modified: Wed, 01 Apr 2026 20:17:26 GMT  
		Size: 10.1 KB (10095 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:fc989035d2688c7051b9064517b02d62ddf826ca62b77e02fc8c313d2f19f4b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.6 MB (227588099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:261834e94fc9dbf43f36d69e8b2c74662819f2c02cbd489e0b288ce16d0943f8`
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
# Wed, 01 Apr 2026 20:16:46 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:16:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 01 Apr 2026 20:16:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd27fdfa418a6103d43b709a1aa9f165f2044348f3094e787d5f275d89c6fe6`  
		Last Modified: Wed, 01 Apr 2026 20:17:09 GMT  
		Size: 200.0 MB (199981156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d7c8e7cdeaba7fe1fa53ebb6837414412841d1a84ab57f90a14bf690e5c57373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2640228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94f11b79470dd0a2eb8a94583519fba56cea00afeaea41ce6b3b9789433987b4`

```dockerfile
```

-	Layers:
	-	`sha256:f9d51cea90630e2435791b422e83a9799a5dcf43a9bd4b81de909c08bf2e063e`  
		Last Modified: Wed, 01 Apr 2026 20:17:04 GMT  
		Size: 2.6 MB (2629981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7074ce3a2b201ff2f23dcb770433d65ac93e354d9e4d4e72460e14a85198605f`  
		Last Modified: Wed, 01 Apr 2026 20:17:04 GMT  
		Size: 10.2 KB (10247 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:c90d5671a25227c0d220369d8617cb0545002f68fc57d541ba7b7e118dcee1e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.7 MB (236715204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1c83f5b282b03ddcafaa9b368d928385525187a41f09196130866422600131`
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
# Wed, 01 Apr 2026 20:51:12 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:51:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 01 Apr 2026 20:51:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6fb1b04a0a70d070de8a04181c7b855a46b1ea4f771660ae7f0783acd4569be2`  
		Last Modified: Sun, 22 Mar 2026 18:43:46 GMT  
		Size: 34.6 MB (34649660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a975ecb2c570f6d088b89fc21bf6363578fa5e414725a0ccbf2d45a72b59652`  
		Last Modified: Wed, 01 Apr 2026 20:51:52 GMT  
		Size: 202.1 MB (202065544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1d9440d8de3e2ef0acfaee78aadf38fad4fd4efc2342229ddbbfce550db0dd1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2638023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26bb89147d4b429b579dc8be96c08e8dd0358694866098d36618125ce7c9e1f9`

```dockerfile
```

-	Layers:
	-	`sha256:ad6ee44b6c027a032d85243098d0a42c126941bfaba12dd877395d85dd562f87`  
		Last Modified: Wed, 01 Apr 2026 20:51:47 GMT  
		Size: 2.6 MB (2627861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4dd07989fbbd0f85902eefde2382437cc0bdfe7b14e5a257ca8cf98d93eccb7`  
		Last Modified: Wed, 01 Apr 2026 20:51:47 GMT  
		Size: 10.2 KB (10162 bytes)  
		MIME: application/vnd.in-toto+json
