## `sapmachine:21-jre-ubuntu`

```console
$ docker pull sapmachine@sha256:cc6a039ec83fce1a884772c49fb416022911f5d1bf34637b671799675e33c16d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:aa197dfe69bf623041a1635d74f7996ad1f85d435386fcb2cc9ff23c9038ad89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89833794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61790b17227b8f192bb519212c4deb9d1a71a6072d2ac3a1e06c7e536e385979`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbea40ab7164f73876a94bf36d17cb1b64793ef01367341cd0455a771b92ad67`  
		Last Modified: Mon, 05 May 2025 16:36:43 GMT  
		Size: 60.1 MB (60116265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0746fba91bf63cf7db57f40cd40c0887b6fcaf440001a4f4b17cc3bbd4d68a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2398271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bafd6eeee6aedf5dd058fd82b5e8208e24da04aa165097ed472270275e9fd023`

```dockerfile
```

-	Layers:
	-	`sha256:882988d61f427b8f01583f549507d0311ff2d598912a4df7fdfb569f92103e02`  
		Last Modified: Mon, 05 May 2025 16:36:42 GMT  
		Size: 2.4 MB (2387822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f236371f102da36585a72e5973660b6e3baee1692ef4fc3b00be71b482e04f68`  
		Last Modified: Mon, 05 May 2025 16:36:42 GMT  
		Size: 10.4 KB (10449 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:333874750bb3b202ae5c5c80597208ce1ac9a06a90ffd8262c356856e9ac0118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88158731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b91582ba7400b1e0eb20e872062bcf46a4a92fa4277cd1f728fbf633327d6bc7`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:09 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:46:12 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Tue, 08 Apr 2025 10:46:13 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8678e318c8ff616971d1027fe8816b9fffb8614eef065b8504c4cddfe44909`  
		Last Modified: Wed, 16 Apr 2025 16:27:45 GMT  
		Size: 59.3 MB (59311773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:306370b9c0bdacf380379078aaf43ac6859c879dba5a62308a7963736990cb6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2398959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61df4d14d5a081acfa4ad28824ad058514bd5a1c414511df80fd20e8acc0ee1b`

```dockerfile
```

-	Layers:
	-	`sha256:0b72b4c18443c723a8c1a5384d9c7092ed7fc2052a0de1b3968fe72cdf86f143`  
		Last Modified: Wed, 16 Apr 2025 16:27:43 GMT  
		Size: 2.4 MB (2388346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a96b7ddf88510bba448099ce6bc1c93190707536af7596bc283e02b57800d7e1`  
		Last Modified: Wed, 16 Apr 2025 16:27:42 GMT  
		Size: 10.6 KB (10613 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:05a0500def3c33d7e265b15ae74ba259edd09abf29d5fbbb19588fb0752d934e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.2 MB (96155480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16a8a37c9a9a553409886a518bd6fcaa8fbcc96acb1b5242465d194fcbd7b323`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:11 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:46:14 GMT
ADD file:d7a12d3d510b1bacf894dbb7d42f36de9391b0766c28643a60d20d3c37a12762 in / 
# Tue, 08 Apr 2025 10:46:15 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7be894b3e11d60e6c310a10016f7c569f1a313b370ab3964114b1c135b1ce53c`  
		Last Modified: Tue, 08 Apr 2025 11:53:59 GMT  
		Size: 34.3 MB (34340867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67790fdbd727b258d4ae07788866f3c8c11e6de1097325cc5a01156bdacfd9f`  
		Last Modified: Wed, 16 Apr 2025 16:44:09 GMT  
		Size: 61.8 MB (61814613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d4f71933d5a41d053547d59899fe61e97c8bd25919226dd6701d781a09180cff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2402311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56934deb59d34cce6849b583cd9502eda7b7f9f2328abcb442531244e71c0de1`

```dockerfile
```

-	Layers:
	-	`sha256:011b9fc20760813e3e2ea4a453199c90463b199dbd8296250b2a31506071012f`  
		Last Modified: Wed, 16 Apr 2025 16:44:07 GMT  
		Size: 2.4 MB (2391787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:771bbcec2322dcf6c6d9a19dbb07116a3c511b59dd4cfab3695881910931f7d0`  
		Last Modified: Wed, 16 Apr 2025 16:44:07 GMT  
		Size: 10.5 KB (10524 bytes)  
		MIME: application/vnd.in-toto+json
