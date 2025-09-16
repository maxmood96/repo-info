## `sapmachine:17-jre-headless`

```console
$ docker pull sapmachine@sha256:160aebf6331d35cfa15d8812ad157c7fc294a245d26bc827765d582c891e538b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-headless` - linux; amd64

```console
$ docker pull sapmachine@sha256:7b7d0afb5dee3dc8b016171947d150977a32d517afcded9c841182ac8bb1123d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82782349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab1a8162da04d77b14ac7f79b829e586513127e3aa7257732dc8937510d27479`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:11 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:11 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28284cb14abc4e8320ef802f56cbcf3516d8ebbd98887c6de69e0eef78510cc4`  
		Last Modified: Mon, 15 Sep 2025 22:27:57 GMT  
		Size: 53.1 MB (53058899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ad62f58808144549a2735ce7efc971402d8b9f9f7dc69570861f183894aacac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2281840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3802564279150055cc8bb334c64192068f8f2c9eb6b19b90b28adfef7d1b2e5c`

```dockerfile
```

-	Layers:
	-	`sha256:a843d6b898f267b7547263210dc22e674ea4bda7f74ad661e3b7d601d8302486`  
		Last Modified: Tue, 16 Sep 2025 00:06:27 GMT  
		Size: 2.3 MB (2271564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f3edce833f8b420c316fe2a7f1fd4bd1177b72eb335fcae39be737cafb3dddd`  
		Last Modified: Tue, 16 Sep 2025 00:06:28 GMT  
		Size: 10.3 KB (10276 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:a1b1458506963ef347bdc99526a81ce9528662f31a8de05b6169b8ca72163ce1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81348707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d55db3ad5425594d885902398b21c7fe50a13b3ed1353ab11149cf173387693b`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:11 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:11 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc3463c3ad49cde6395b57b4e8cb3965062c09ec4d0d1acaa6898b1cb0b8726`  
		Last Modified: Mon, 15 Sep 2025 22:26:39 GMT  
		Size: 52.5 MB (52487390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c55075ed748f31bb6cc5301cea6bd68fe9b458f4dd430cec1d6adc58010a5522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a3708c8b184d0614adab86da6096b572aa2ce35c182e7f93c7128b155516389`

```dockerfile
```

-	Layers:
	-	`sha256:09be9d3f728cc30ac9dec989f8e34738a8995b0fb101af64949676b55e7ffe29`  
		Last Modified: Tue, 16 Sep 2025 00:06:33 GMT  
		Size: 2.3 MB (2272071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b7a687b7d2d07db9b49e43d9e1fb89e97bb13fffbd91d68eebc312cce3c02ef`  
		Last Modified: Tue, 16 Sep 2025 00:06:34 GMT  
		Size: 10.4 KB (10428 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:1a03f842a829cf0bbb8c44aad9e5847f6b030f36b784196c383399dfb8c1b3da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 MB (88395167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d0674861f98a196770907156062bed2ccc5d1a750bcecfa66af8daa4fab697`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:11 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:11 GMT
ADD file:55e5af389c76b79c77275691d488810a1fd875fe7e47b4b14a8b70f1230bf1a2 in / 
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5128fb40eedc06172c4cc2920b45ddb874f5b42c161d0a777ed53f0b9f80b8e7`  
		Last Modified: Tue, 19 Aug 2025 19:17:46 GMT  
		Size: 34.3 MB (34329533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace1c69fd33c4767295091c4ac5a88d64ba62b22bfe1fd37a018d76e2cea73db`  
		Last Modified: Tue, 02 Sep 2025 05:16:51 GMT  
		Size: 54.1 MB (54065634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b215d1471c89b5414dce403108a6db7cef186b09ee4bd13232b36f07a1dce8f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add6cb6511c6e29c4696d4bd70ba6583a42c3c2a2f182d9a4dd50a65b6215ea6`

```dockerfile
```

-	Layers:
	-	`sha256:e0873a1964b3de6c1559281e7f5843bb46deceb7a7f67d0d21ca6af5f1847894`  
		Last Modified: Tue, 02 Sep 2025 09:05:13 GMT  
		Size: 2.3 MB (2269560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a69c4ebf88a8f0ece0e4ff2d112baf548ee9067833b54d3b8d537e426b3e62f2`  
		Last Modified: Tue, 02 Sep 2025 09:05:13 GMT  
		Size: 10.3 KB (10343 bytes)  
		MIME: application/vnd.in-toto+json
