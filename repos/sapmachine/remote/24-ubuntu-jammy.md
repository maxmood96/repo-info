## `sapmachine:24-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:79cf923a2221c63c2541cc06ef805c8b8d19816abb2dcbc4a4c113bc0c022001
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:24-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:1a7443e23838e1640fe2ea4e2fd061945d1c4dc489c588b46bdab71034132d12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.6 MB (261581971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceb9a34625109cf5b9045e3b8882db28473d8351572ac3c96d29ca72ef39eafb`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eaa6ccb3ac83f0c0cfe0505f4e5180b521d8ab32cefa342ef2228aac280c02f`  
		Last Modified: Mon, 05 May 2025 16:37:05 GMT  
		Size: 232.0 MB (232049357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:34021467e76d52a92cc70197a6248256a8b25414f7ec845ef71fc722cafbf156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2496964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b21e12f9ba0160333bba2f25bfe5ceba8e9b24981e809aefa9a7d8a1da6699a2`

```dockerfile
```

-	Layers:
	-	`sha256:0e0f260e40fc0d8d8bde0ce61575985a27b91e4b5dbd1069ab60faac7e0d9b1d`  
		Last Modified: Mon, 05 May 2025 16:37:01 GMT  
		Size: 2.5 MB (2485551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de7c1f88d95231cafa80469a404b90e7d338401c0cc312d02b5ec10f302faf00`  
		Last Modified: Mon, 05 May 2025 16:37:01 GMT  
		Size: 11.4 KB (11413 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:9059e45fb343695509da19a081552ec10c863913d073243e1b078fd1c0e0ff31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.3 MB (257268044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99f76e046707f6e7c03975419bea163c029f59b601b68cd74cef617ac0feca5f`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Thu, 08 May 2025 17:05:00 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345671845e42151de24001b3e97f8918c0979982b57804f4acc3ca1ce1fcebc0`  
		Last Modified: Mon, 05 May 2025 18:27:13 GMT  
		Size: 229.9 MB (229913833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6992fd7131bbb0c07c5ba437eca38fdafa3ebee75548ae4403efb636de9a36b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2496939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9bfb9b71eeee4292dc8481c692ef7d85ab9db9452121aca8edc3739e8af7dbd`

```dockerfile
```

-	Layers:
	-	`sha256:9750609d77fcf7d56ddf3c1368dfa4042311ab44727afe20dc315a1c547846ed`  
		Last Modified: Mon, 05 May 2025 18:27:07 GMT  
		Size: 2.5 MB (2485326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb4feff8715870a1fffa9b7a0b8258e19dca2bcf7f905a5edc79077f3964f2d5`  
		Last Modified: Mon, 05 May 2025 18:27:07 GMT  
		Size: 11.6 KB (11613 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:e8adfa3a480dc21ff07015edb29f6ecba4d2f826391d4a054157bff2d7983cac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.7 MB (267695039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fecc9926da2d72b93659d269e2864e877edc9eea1a1243e75b8e1a0c6acd6165`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:f6d72fdda03fb8754d82331b1f726d49b6b7d2d850ad2d1dfc2de6e1b365251b in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:95ba4619a43d3f4f7f5ee2c8fbe313d19bb9c0e9ca5fa9efeb7b93f942dcf377`  
		Last Modified: Thu, 08 May 2025 17:15:30 GMT  
		Size: 34.4 MB (34443215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d2bdec4f283c2ec8b082af46debcacb3bc75b18e45b1374bbd32fe37a7e6ab`  
		Last Modified: Mon, 05 May 2025 18:17:13 GMT  
		Size: 233.3 MB (233251824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ee6a1c1179eb28dc82e3370b24774089e9250bd65716086e2ae75703a02c7172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2498521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6948f2fe838b529e2000270ceea994de21901897eb4591fd03f645af3f28636a`

```dockerfile
```

-	Layers:
	-	`sha256:75810d77ab8b42ba031cdfae277996c538ce951d1fab47796daae62871cb5a6e`  
		Last Modified: Mon, 05 May 2025 18:17:06 GMT  
		Size: 2.5 MB (2487016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4fc4652cad88029089017b56669608bfae22b86f41788a6ed65c0e382d17488`  
		Last Modified: Mon, 05 May 2025 18:17:05 GMT  
		Size: 11.5 KB (11505 bytes)  
		MIME: application/vnd.in-toto+json
