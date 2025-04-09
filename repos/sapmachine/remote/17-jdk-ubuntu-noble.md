## `sapmachine:17-jdk-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:c085f0b5f0d6b2469408d2d1bef5a7f38f8d46fcd9847ba7263c8a085fdc8961
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:1f2b890c3888b39a8e7f72f162cf80a6f3b8eb4c01516f4b1872c863cee783ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.0 MB (230030387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a66ce73acc16028a461931164937dab02430f8485c3cf73ddb2975415aa2e75a`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:16 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:16 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 13:39:16 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a5aae93924fc7a5d5585c8ddb838af684c2037dedce2b0b4afe38f8f5aded5`  
		Last Modified: Wed, 09 Apr 2025 01:21:45 GMT  
		Size: 200.3 MB (200312735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:09d04c113d489ee39935583615608bfe26ce6290915237283eefe05c3345e590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2481804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:567b41206aecd8bd8a9f4da54b57ad48f9a1c0e8ea41521b2a714cba64b9e4cf`

```dockerfile
```

-	Layers:
	-	`sha256:a1bf9e777a9a4e825e2ffbad93265d55f51dcd549086b416ccd8d17908e50c57`  
		Last Modified: Wed, 09 Apr 2025 01:21:41 GMT  
		Size: 2.5 MB (2470410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b46bf1cbbbef4718c62c9c544ab69d7f88fbe75331682623952d77241f9eada`  
		Last Modified: Wed, 09 Apr 2025 01:21:41 GMT  
		Size: 11.4 KB (11394 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:c413588edd46e811d2457009cd3cebc3be6144e0307445da7b639542cbfdfe7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227912753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5480e0577e0b0e4a9fd961303af6ecd8adb512c1e3cc3464f774fa36562bb7ad`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:16 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:16 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 13:39:16 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db7c6d66b9c01b19773bb669f2f9ff2003dc386b3199616bc51671da7a8fabd2`  
		Last Modified: Wed, 09 Apr 2025 09:40:14 GMT  
		Size: 199.1 MB (199065795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b1c490f108367c8c9345c73a5b25351f4bc40e5167dcbad436449607dd42f967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2482566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f4477d0132ea2b07226580d3d5f0cf0803053110419f6452e919b578635fe5`

```dockerfile
```

-	Layers:
	-	`sha256:4f2a914e7391b767bd01e6f016e2f52c92d5f72d3965ab6110c3ec9802ea74c5`  
		Last Modified: Wed, 09 Apr 2025 09:40:09 GMT  
		Size: 2.5 MB (2470974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9325d39ac78b8b8886b175e29660a222d2aac4789e8a3732609efa720f66ed4`  
		Last Modified: Wed, 09 Apr 2025 09:40:08 GMT  
		Size: 11.6 KB (11592 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:97948ee61e3cdbff1a733580449033c04b6a824f687cf8e5509f5253677cf5c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.8 MB (235841893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d5cd0260ca3af1cf4ba74ca27e25034e914965a6843faed2b03a64ffed3a9da`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:16 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:16 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 13:39:16 GMT
ADD file:d7a12d3d510b1bacf894dbb7d42f36de9391b0766c28643a60d20d3c37a12762 in / 
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7be894b3e11d60e6c310a10016f7c569f1a313b370ab3964114b1c135b1ce53c`  
		Last Modified: Tue, 08 Apr 2025 11:53:59 GMT  
		Size: 34.3 MB (34340867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:446b7d82cf78096a1b330c5fe9249314f7e5e67dce4f868c1561b66874974966`  
		Last Modified: Wed, 09 Apr 2025 07:10:13 GMT  
		Size: 201.5 MB (201501026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e77874ecf0a734354f38b4d0f0ce8a0ce98b98c7857e88e76c205234cf752e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2483937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee8c4d4a9a900b44dedfc6c4a0db91203d3d3e25a217ddc06a352a3f2c1a1405`

```dockerfile
```

-	Layers:
	-	`sha256:201fb1c07c83b52907cde726fde8e72add6dc24175d7cb03883c84de777f734b`  
		Last Modified: Wed, 09 Apr 2025 07:10:07 GMT  
		Size: 2.5 MB (2472451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a34e57524e53d55cdcc3b3bbb9a7067ca7c2c8b361025456bb578afff5dab853`  
		Last Modified: Wed, 09 Apr 2025 07:10:06 GMT  
		Size: 11.5 KB (11486 bytes)  
		MIME: application/vnd.in-toto+json
