## `sapmachine:21-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:f85669ae33cecb2ace9c2d59b555b298e474a66b3141227c224527ad2ce35ea8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-ubuntu-24.04` - linux; amd64

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

### `sapmachine:21-ubuntu-24.04` - unknown; unknown

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

### `sapmachine:21-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:036ec684b972cea186b48f935b55de28615115fc85f9e949455c6faa85928f64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.2 MB (242175645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2987f58325fa8eff02e2a9e5e9db71bef0df281aabf881a35c85e34bc8bf84a9`
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
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19c229e63b62d60c56ac00bc3ed914323d95d6ac32ce83864ec017892c77fb5`  
		Last Modified: Tue, 04 Feb 2025 15:25:48 GMT  
		Size: 213.3 MB (213282047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:52d99afa147f3531eed8a416b3fcc33a984707af9f64ffcf93982a34522e25c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2490619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa70bc44cefee8a6e2723cea53d6d17711b7127cfe27f50ade42d7941159edc`

```dockerfile
```

-	Layers:
	-	`sha256:743fb64faf6b1bdf9f76c087c39d683b8dcc317919604620e03ec89e991b5d52`  
		Last Modified: Tue, 04 Feb 2025 15:25:43 GMT  
		Size: 2.5 MB (2477028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75e655863a60af3fb9c67d5758c8b27d3164c62348c7d9ef577a38746d398762`  
		Last Modified: Tue, 04 Feb 2025 15:25:43 GMT  
		Size: 13.6 KB (13591 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-ubuntu-24.04` - linux; ppc64le

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

### `sapmachine:21-ubuntu-24.04` - unknown; unknown

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
