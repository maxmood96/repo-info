## `sapmachine:17-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:52e0d6c70dc0125db45cc3694ecd81def1a851c8d01e2ba439a9929bb7529b60
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:4624e394ee9a1d45ad33969f955193c733a39e47fb4873620989a52c94c942c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.1 MB (230121496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66e8e514fb1bef25d002c01dab82c8db3baa3f7b90666407a40dbd2453bfb9ae`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 08 Apr 2025 10:43:12 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:43:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:43:14 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Tue, 08 Apr 2025 10:43:15 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27cd71e72be373c3f54cc32ba95ca16fd3333e72b8de8753d1a458409211c71e`  
		Last Modified: Wed, 16 Apr 2025 16:14:31 GMT  
		Size: 200.4 MB (200403844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5f40b1b10a38f005257e6b10c2787c9ccefc29783f7d0511803c0542fce51b28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2481804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8601714bc2733e5672baa1880ccfec19c06da858443d432b75c3413ad52bc75f`

```dockerfile
```

-	Layers:
	-	`sha256:7b67d6fa24e1e03c4e39e80ecffdcbd0f92de43568a8c69702490ffb0fed4907`  
		Last Modified: Wed, 16 Apr 2025 16:14:26 GMT  
		Size: 2.5 MB (2470410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2c3801e6e9a47172f3dbe816fa6740a833d33c55d0c7efe81df372bd5990439`  
		Last Modified: Wed, 16 Apr 2025 16:14:26 GMT  
		Size: 11.4 KB (11394 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:8852709d2681218a559fa43992c968a07a689481d86e0e5e36980f26bbef0715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.0 MB (228006270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:264559d5ff66f066428ce2867e55b7e757827ee48bc4cc55a44d6b140ed87064`
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
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76e6801b1af8b10902a27a62fb55793f276be9bd3d17682778b5885193e36f04`  
		Last Modified: Wed, 16 Apr 2025 16:36:46 GMT  
		Size: 199.2 MB (199159312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:63ddbc690cd0ba377a94fbf5bfe2a9bec1cf4aab0e393df52c12720f1f021fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2482568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b0af529f99c31c52f93f3ff72c6801cd55e1811ad3aa1a11d6d2e0a9ce9b6ae`

```dockerfile
```

-	Layers:
	-	`sha256:958a0ad445ce8fd74ad715d1f2a99a850120ff9ca2b00f2d269084b249ae3290`  
		Last Modified: Wed, 16 Apr 2025 16:36:41 GMT  
		Size: 2.5 MB (2470974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c87891a93ccabcda579d21b72e26f1666f805f51db37651b70d16a646eddd960`  
		Last Modified: Wed, 16 Apr 2025 16:36:41 GMT  
		Size: 11.6 KB (11594 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:2d1b7b3500c3e2cd989b60b597b1189d79a7e01cb7e0a7445b36b4ac279def16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235931838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdae18fb8dc59725d0862233cc609cdfd562d0f72b9442a1ea12f1ba37b77c77`
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
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7be894b3e11d60e6c310a10016f7c569f1a313b370ab3964114b1c135b1ce53c`  
		Last Modified: Tue, 08 Apr 2025 11:53:59 GMT  
		Size: 34.3 MB (34340867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d187a84931f54bb2877693e3a08d8a7e5391ca89e62bf78de809f62ed8e6748c`  
		Last Modified: Wed, 16 Apr 2025 17:03:00 GMT  
		Size: 201.6 MB (201590971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3477c293d07a3eb3cc4af12b1d815ef762e2d1acaeed8905cf201b6fc5ab0ee6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2483937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ab8c9efe30db4a51b796debdbabef04f22b4d46fa322cdfcbea422451d0abf1`

```dockerfile
```

-	Layers:
	-	`sha256:8af341d0447879575f4abf74110c6ced8f685eaa9391ee38e0db7088b6038984`  
		Last Modified: Wed, 16 Apr 2025 17:02:55 GMT  
		Size: 2.5 MB (2472451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a36b64b5da4696bd243d6114a8e156254cd945105ce0c57550bb0cd48440c4a`  
		Last Modified: Wed, 16 Apr 2025 17:02:55 GMT  
		Size: 11.5 KB (11486 bytes)  
		MIME: application/vnd.in-toto+json
