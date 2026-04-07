## `sapmachine:lts-jdk-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:933625462d3ace39d3f0f834351f6ee2b3b5ca55c6dbb450397e0fea18edff3f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jdk-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:e08216afa98e4d8faae6b557343a4c22579c7d4757d61539bec91e801d0e4aa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.0 MB (250017106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a47a9d10ee72d2284db019a779f268b387eba6a59c39450db7967a0d95c58dc`
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
# Tue, 07 Apr 2026 02:32:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:32:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 07 Apr 2026 02:32:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bfd60202d56614061c448c2fddc51d39ed77c964119707262c8b6081003ebba`  
		Last Modified: Tue, 07 Apr 2026 02:32:58 GMT  
		Size: 220.3 MB (220283647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:49635dc864b64640b38803073d38b17e1137dc83064d403629284ff57527f0e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2360528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1e0dbe96888c9a0a49d44b3bce35eaae594e776efe41b9a43d77078b1779a01`

```dockerfile
```

-	Layers:
	-	`sha256:6ef699bf54587c6c823e7e3ff7d09be56a28a18600cdc257ebd611f01a33c701`  
		Last Modified: Tue, 07 Apr 2026 02:32:53 GMT  
		Size: 2.3 MB (2349263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0aee051664b01423e53c9d4146719639551244e7d58f2b4755e1ae8fae660ea9`  
		Last Modified: Tue, 07 Apr 2026 02:32:53 GMT  
		Size: 11.3 KB (11265 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:ecf86fcc596be6f2bd0df059f2adc6e1f8292b7c21986fa5adc63319cd9e3b60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.9 MB (246942660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfd1426d2ba60653ecd2668c6878f32bd5f912a7f6c0a31e09010acaad6308d9`
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
# Tue, 07 Apr 2026 02:39:14 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:39:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 07 Apr 2026 02:39:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b05abf4a2f7b919e5752c22457ae855bab575e876c7f04c7649e553f5bab7b46`  
		Last Modified: Tue, 07 Apr 2026 02:39:38 GMT  
		Size: 218.1 MB (218068585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:215b877e55b96ad2039d17f588aa72a79c94a94decf657e85ac7ea2b1cbb899d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2361256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7ce92f2b451c34a122150154f9582e1a45f6ff41cbbfa94bc5a54e6898c60ed`

```dockerfile
```

-	Layers:
	-	`sha256:5bea21b93caebcd0ec9c7f6582cfeb921951100438dff7f7ca0cdceb58f14b9b`  
		Last Modified: Tue, 07 Apr 2026 02:39:33 GMT  
		Size: 2.3 MB (2349803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c256968612bb8eed2d05df2784aeb9b292e1ad63dff433b7c17accd1baf7bbb`  
		Last Modified: Tue, 07 Apr 2026 02:39:33 GMT  
		Size: 11.5 KB (11453 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:4226192c94231dfe3004442003be99a1220a05a97f6b40984acbbf02f2067053
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.3 MB (255280785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:535531a9004861745f6d05d14dd8472f9e90dba6838824cd54b65eaf995c41c4`
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
# Tue, 07 Apr 2026 09:04:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 09:04:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 07 Apr 2026 09:04:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2206a81f65df3147f8c62d4c01c47495515dae16f93ce6845cd7cdacdd206f1e`  
		Last Modified: Fri, 03 Apr 2026 15:56:51 GMT  
		Size: 34.3 MB (34313334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df1bdcd5d32d93659b4cc1efbb163d14aea3a6765cd2fab23a1278ed7863faf`  
		Last Modified: Tue, 07 Apr 2026 09:05:02 GMT  
		Size: 221.0 MB (220967451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:06b46a481c8bdd0d2977569c35fde5ccde13cfac60c059c95d595b5d2f52e232
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2357485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:210851edbac5a095449665be1fcb3283d8b01e3c7fc68d04d58c49334c57172c`

```dockerfile
```

-	Layers:
	-	`sha256:0527af0a63244ccbbe4a295260b2428704f5cc71dab7be065826db548020a8c5`  
		Last Modified: Tue, 07 Apr 2026 09:04:57 GMT  
		Size: 2.3 MB (2346134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a682ae5cdbc2a90818516cbf47caa9016213ecfbdc44d8523d37c71cd5e3c8a3`  
		Last Modified: Tue, 07 Apr 2026 09:04:57 GMT  
		Size: 11.4 KB (11351 bytes)  
		MIME: application/vnd.in-toto+json
