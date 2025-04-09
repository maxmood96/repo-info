## `sapmachine:21-jdk-ubuntu`

```console
$ docker pull sapmachine@sha256:667423e80da25a2ef57ff78bb1e65951718434960dfc5712b541d9e975808341
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:1be15715a6ff2a352611e6a1207a83850625bdc25858542a80c21f8629246fe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.8 MB (244750763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2cc1c97451ed2290199df44fd11296dc76c149149288f3134aaba323f0dbba`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:13 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 13:39:13 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b9db49865987edfbb22b6f45f7a915ea2ecc1b906fed8e6dbe1fcf31e4f1f6`  
		Last Modified: Wed, 09 Apr 2025 01:21:00 GMT  
		Size: 215.0 MB (215033111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b8540f880c7bc66648d7b35788bc7ee2d3e3c671532e1e0db29960364a3e161e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2487526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9af8047ef1059369101eeff8a8f9756816c632956d6e13119e48c063df43f139`

```dockerfile
```

-	Layers:
	-	`sha256:d9ae443d8d1155ebf8baa36dc0130ac7182c7193270286750a1eea2327d8ce11`  
		Last Modified: Wed, 09 Apr 2025 01:20:54 GMT  
		Size: 2.5 MB (2474207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcee01073048aa664d53b6f31d90b6650a178322cfb7377e0ca183cdce27af1e`  
		Last Modified: Wed, 09 Apr 2025 01:20:54 GMT  
		Size: 13.3 KB (13319 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:07dd26e6c452afd66e83ebcf7666822a6a36f19d0a83bb0f12e49a40b176cccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.1 MB (242133355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a0411468ffdd5e9410453eb3b8eb0cda35c4d97e437d561efbbbbca4d4750a3`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:13 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 13:39:13 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2458e0940e0b32dbe4c48347f724a8b942785769106fd400c6d7cee07337bd5`  
		Last Modified: Wed, 09 Apr 2025 09:29:04 GMT  
		Size: 213.3 MB (213286397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d4a66e0030a2572bf2b92029088592ae0112080cfa627f1e9245e090f546a9b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2488432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ccbf6e82ffaa8205d546db5214dd763fba737df38b080a2c1c8a5ca738fea91`

```dockerfile
```

-	Layers:
	-	`sha256:5ea09d69554eafb9e89051cab6d941162aa998d5df22baef4a6cf1c4263fe467`  
		Last Modified: Wed, 09 Apr 2025 09:29:00 GMT  
		Size: 2.5 MB (2474843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cf6e09bd1e54419ad1fde1af5f4863083eee7d9425025e1296bb549aeaff0c7`  
		Last Modified: Wed, 09 Apr 2025 09:29:00 GMT  
		Size: 13.6 KB (13589 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:cd21db3715cb7efc29d20358f83b271cd9f20ecbb927048bcf40e8c19bc63fdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.8 MB (250790358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d10c100d65a81e3eb927624dac12ac2cbbaeaf0afe58327c68b15266a84c27a3`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:13 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 13:39:13 GMT
ADD file:d7a12d3d510b1bacf894dbb7d42f36de9391b0766c28643a60d20d3c37a12762 in / 
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7be894b3e11d60e6c310a10016f7c569f1a313b370ab3964114b1c135b1ce53c`  
		Last Modified: Tue, 08 Apr 2025 11:53:59 GMT  
		Size: 34.3 MB (34340867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2984f7ade87f68b90f93852ac672542b31661400abf67b80ab6f7c4339572276`  
		Last Modified: Wed, 09 Apr 2025 06:51:50 GMT  
		Size: 216.4 MB (216449491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c470b0d8212324fa76d78a11d5ee3b5da1a1ecbdf343188cf577913a525bb225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2489731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68c287c1d38c77855aab20a8d6eedc9608e7352910cdfa396003ca762075a5c7`

```dockerfile
```

-	Layers:
	-	`sha256:2ae1467a84ff0a2a5b6f3dc44de3bf3f76d6ac77879b7f3393ccb3a5dcd47351`  
		Last Modified: Wed, 09 Apr 2025 06:51:44 GMT  
		Size: 2.5 MB (2476284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:568d2569450865f0ed523dd1eff1cad8bdcbbaa544b2232aace02bf6be8a741c`  
		Last Modified: Wed, 09 Apr 2025 06:51:44 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json
