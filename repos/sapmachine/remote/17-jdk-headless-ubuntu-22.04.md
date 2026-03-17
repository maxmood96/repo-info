## `sapmachine:17-jdk-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:11195c9ca56ad13368bfb7083c1c2217119b55d4794a209592a1f68a24b58d4e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:656bdf6126a35f8691ee7706259da66839eed195f9abcdbc70c32ef337aa60d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.6 MB (229621403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1168e051fb2f86eaacc82eb1a6533d1f42e9a72a38db08499ac77d4e7b2ca5ff`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:25:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:25:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 17 Mar 2026 02:25:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15048911ecd93e3d696a1abbf2f1aaffad7233d42e272c1be6bb210fe2b11b43`  
		Last Modified: Tue, 17 Mar 2026 02:26:09 GMT  
		Size: 200.1 MB (200082883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c553e7e4fd31583ea1a458df86b6236e298589abdca2adbcfa7bc06ba5310f80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2387044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfa2fa8ab31e36e88926ca8a00ea9c1de2a17c62b688bd4157682f76f7376c68`

```dockerfile
```

-	Layers:
	-	`sha256:54e4bb7046bfc69a0aeaabae54ffff5c78b3a3c643fe2db206148182c4b9a724`  
		Last Modified: Tue, 17 Mar 2026 02:26:04 GMT  
		Size: 2.4 MB (2378155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab254a9ddd44cde7464aa1d1f96ba6ca47b75308ae18bdcbb285e1418cd29173`  
		Last Modified: Tue, 17 Mar 2026 02:26:04 GMT  
		Size: 8.9 KB (8889 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:afe6f1f7ba35e86c52014cb132a77122193a5878f5197f65c05fb99bb2ba97b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.2 MB (226156606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438b03441241f3924e276d67bdc8535cfe0aeef6e7534a707b9416f1bae8ce0d`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:31:54 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:31:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 17 Mar 2026 02:31:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2bd5ad92b7c70aff043bfa27e383ee08190c1acc945357592b38d94bdc60ac`  
		Last Modified: Tue, 17 Mar 2026 02:32:18 GMT  
		Size: 198.8 MB (198767581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b62d7b7d3405f6715d8a1f5ede37c89eccee382cecac939c26d247a171a0add4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0ef268c738249fead85be96ceb25d84308b18e184c6aa2895dd88324d3e63df`

```dockerfile
```

-	Layers:
	-	`sha256:727d105ce35af38ff8cffc991a3a80249e874e1ad7adfb7fde085e2ba087569d`  
		Last Modified: Tue, 17 Mar 2026 02:32:14 GMT  
		Size: 2.4 MB (2377827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4355ea7b0b98472658e6fd202ffa841c97cd59fced79d31e0ef231d477f311a9`  
		Last Modified: Tue, 17 Mar 2026 02:32:14 GMT  
		Size: 9.0 KB (8994 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:d91dd1be79a492eec96db93994e20fbed7f97fc6558f4d4a0fe4c6ef7431c24b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235122932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d520389f5a60cd5bc32b0ac7a70c39f306373dae5016e0a770ad8bcf16830b4e`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 10 Feb 2026 17:41:33 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:41:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:41:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:41:33 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:41:39 GMT
ADD file:0418bf4995f9b54380cc1e509e3f7d65bb07aed9a367528d0b1084f0a34f3bf3 in / 
# Tue, 10 Feb 2026 17:41:39 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 21:38:38 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:38:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 17 Feb 2026 21:38:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:95401e425d899946469007a0ce4b02622cf84a67cdd684aa25d61d472fffc38f`  
		Last Modified: Tue, 10 Feb 2026 18:13:52 GMT  
		Size: 34.4 MB (34446102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf050a5075926786411da94801eab10c28686bcda8fcaf72345b8234af176f36`  
		Last Modified: Tue, 17 Feb 2026 21:39:35 GMT  
		Size: 200.7 MB (200676830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6c788796c9a883340199f0d0bd1a554bb5eeaedf3f39079958314bb43f2bb2ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffcb6a6637ba7822c4ce6ad911be8cf441977652e93a54a219d42319371ca0af`

```dockerfile
```

-	Layers:
	-	`sha256:c8e70085625ba90963d812bd03e313e27c4269772533580d7af22f539da1b12c`  
		Last Modified: Tue, 17 Feb 2026 21:39:29 GMT  
		Size: 2.4 MB (2375651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f532e650f287eaf79ccaa70b0f9dcd1b0f567eb7e0dd9929762b1119b6fa723d`  
		Last Modified: Tue, 17 Feb 2026 21:39:29 GMT  
		Size: 8.9 KB (8934 bytes)  
		MIME: application/vnd.in-toto+json
