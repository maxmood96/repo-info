## `sapmachine:jdk-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:4215b1e1b5f04cf5b786d05b1b85e3d55bea3d76f349495d5c4792898c6a88ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:dfee474044c6a4afdd153c552cc7f210f66783a8294a04ac50344fc714b6b795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.9 MB (254912702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e304372aae7157ec8fe269d975c74acdc9ad5e78bd10e670ce6645c9f6ce89d`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:32:24 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk-headless=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:32:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Tue, 07 Apr 2026 02:32:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93987bded74223b67f1bf0f6254cbe8cdb251b19ef13c3f7dbfe6fd7d1d46924`  
		Last Modified: Tue, 07 Apr 2026 02:32:48 GMT  
		Size: 225.2 MB (225179243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b5c164a20b712b70be08afe5ce4b8342fc7e9ef04a0909b581dbce22f3ef14d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2356405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3a5a3fc5dbb5928453aa04b54e460ebb2e402bdaa6c6aa7231a6afe528a6e2c`

```dockerfile
```

-	Layers:
	-	`sha256:cde281b4b0d8ca6cbae61539e4d24a1ff5e912ae476fe0bbfac9a13d4af64063`  
		Last Modified: Tue, 07 Apr 2026 02:32:43 GMT  
		Size: 2.3 MB (2346248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ee90f30a316e2d41e62fada2f34ad75e72ac7035a8148b3947ca9627781c496`  
		Last Modified: Tue, 07 Apr 2026 02:32:43 GMT  
		Size: 10.2 KB (10157 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:0ec13062013f53d3cccfe2fef764a458cb99eb4447bc708dc19b65103d8e3749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251912979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25e688c4bc909c3004ed7a3004dabe9a761385ff9965cfa41c8ede9f5b91af24`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:38:25 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk-headless=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:38:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Tue, 07 Apr 2026 02:38:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda832ef949485d39936ee75e1c17cdea8196901b694952f7174e8c83555676c`  
		Last Modified: Tue, 07 Apr 2026 02:38:49 GMT  
		Size: 223.0 MB (223038904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2831afd0d343218bafe9d560fd38891d4a360a2204283be1676fc110816b1f75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2357061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821c54f76b8b25569c43087e3377611929b35c9252e452a97f9c828af516e6da`

```dockerfile
```

-	Layers:
	-	`sha256:8aa48069978504f65f7df8827488a24bde553df79bbbf9207bb98a575e34f6db`  
		Last Modified: Tue, 07 Apr 2026 02:38:45 GMT  
		Size: 2.3 MB (2346752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d921ae31765a9279d965eb9153d9d4cd840807559a6223751e1f545c38ac4168`  
		Last Modified: Tue, 07 Apr 2026 02:38:45 GMT  
		Size: 10.3 KB (10309 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:8016cb93a0ce92f764e4a11092dbeca0d68fd6a89b8816910843f7bfd9f979ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.5 MB (260546941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1824bf788c512aabbc0e2f25e6b25b698fd4db8ea03faf7f9db88d5f9e85c28a`
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
# Tue, 07 Apr 2026 09:00:38 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk-headless=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 09:00:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Tue, 07 Apr 2026 09:00:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2206a81f65df3147f8c62d4c01c47495515dae16f93ce6845cd7cdacdd206f1e`  
		Last Modified: Fri, 03 Apr 2026 15:56:51 GMT  
		Size: 34.3 MB (34313334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720a2eeb7423bcc3f0cea987fe3dc0f481ceda29b07604981ae3a636c47015a4`  
		Last Modified: Tue, 07 Apr 2026 09:01:45 GMT  
		Size: 226.2 MB (226233607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5d9fa0f8e6aaba5ca11a1e330808a63e3b86b760c18af0f99a355adc8526fff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2353325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6613e5b468e1f0de45f2dc85eb565c3256adc94eebcac73ee2c73a738b3e07b4`

```dockerfile
```

-	Layers:
	-	`sha256:54f1959b3b058f3c8d90a31294fe8ebca1b37fd6e18f17f0bba67d0d462ccc16`  
		Last Modified: Tue, 07 Apr 2026 09:01:39 GMT  
		Size: 2.3 MB (2343101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b0a372d4dbb12d9dfbff6541c638a6161733d38bfc7130b82c1643a66e8144b`  
		Last Modified: Tue, 07 Apr 2026 09:01:39 GMT  
		Size: 10.2 KB (10224 bytes)  
		MIME: application/vnd.in-toto+json
