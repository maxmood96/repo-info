## `sapmachine:17-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:4ddd4f9a31507e65273c2bad2c92aeb8ede44db91b4fd41de39bd888fc1035ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-ubuntu-noble` - linux; amd64

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

### `sapmachine:17-ubuntu-noble` - unknown; unknown

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

### `sapmachine:17-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:83138b7d93372d561fe4b316eb3e14b472cd19daeef73a88d593780371b87037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.0 MB (227956926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f9d03957b442828b4f2f888f02cbe5f999c10295240be5acbc635b051793b9`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd80ff3e3b5876612fd701517ff3f7742e3bee19aa259dc87fbac8fdeee37ee`  
		Last Modified: Tue, 04 Feb 2025 15:34:02 GMT  
		Size: 199.1 MB (199063328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0c26e1fc9c20542eba68e6f0a38c7a3126ad6d5db823c08c63c86cd3b372ee17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2484753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45088c5803994190bba16c96b7d67310a11cf9f6a7f3272a51f43a08ac30fbb1`

```dockerfile
```

-	Layers:
	-	`sha256:5b1181f3bf8e6b42828793036ec95f03e21697034e702d3f39f42828f8acf5fd`  
		Last Modified: Tue, 04 Feb 2025 15:33:57 GMT  
		Size: 2.5 MB (2473159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79810ad6194f9173fe5b9f0aef0fde4c102b72a22556bb4c34e24794f69689ba`  
		Last Modified: Tue, 04 Feb 2025 15:33:57 GMT  
		Size: 11.6 KB (11594 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-ubuntu-noble` - linux; ppc64le

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

### `sapmachine:17-ubuntu-noble` - unknown; unknown

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
