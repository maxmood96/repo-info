## `sapmachine:17-jdk-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:f0ac04d2884d471f324b023bd3932197110d668034b3da38937100aa937fd57b
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
$ docker pull sapmachine@sha256:e5740d7c199dbe4c39a57a2c7f1576e1b05bf1c5b1c8ecda4866e9dffbd625d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.6 MB (229620254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e941335737a9d1f32616f7de57d23f6c1f461dec412684eb4ea7cebc3ad8dc9`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:35:40 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:35:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 17 Feb 2026 20:35:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0d43986bade126a2803d508dc1a72f0df124d70d4ecd11a8425998ae90a324`  
		Last Modified: Tue, 17 Feb 2026 20:36:01 GMT  
		Size: 200.1 MB (200082888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4c2e16bd015b7a4ebcea43baa1ef658dca063c40a6a012ff5c2dcb04e0f23d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2387045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b66ccd999804de8cada87ea96b06eae384be96ee1a74b74dea553da7a253c39`

```dockerfile
```

-	Layers:
	-	`sha256:e863f50c559992850aee1460f1db6fbe601d0e154d2f442f4de4a4ca8f6bb882`  
		Last Modified: Tue, 17 Feb 2026 20:35:57 GMT  
		Size: 2.4 MB (2378155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5528989a2b34698422e3c24d0dac8c64a5d5774e08acba3bf4b67d16a1b48332`  
		Last Modified: Tue, 17 Feb 2026 20:35:57 GMT  
		Size: 8.9 KB (8890 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:1ebedd166c94ac0eec1c6de94a9fda1cd0270854e8ab154f0f547c0cbabacb96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.2 MB (226152001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a804490187004bd89f8f9cedd9f3bdb6e0ff19744fca9658c31fbbbad9c2b68a`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:34:39 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:34:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 17 Feb 2026 20:34:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b012a644bea8650d8dc31f6c0207fd4a38d35034e2d9af809590236538dcddd`  
		Last Modified: Tue, 17 Feb 2026 20:35:01 GMT  
		Size: 198.8 MB (198767057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:82e577684925872c116e005b5560ce87c133746ed163b6111643bb807b5389c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b122f7d70cec37293d301a496a383a1bd72334a6a615390d1da027e54e85a818`

```dockerfile
```

-	Layers:
	-	`sha256:5c0d2b4b0262407cf16fc4f01c5de7f7c40b36e8f167c83873c90be5a9bd8039`  
		Last Modified: Tue, 17 Feb 2026 20:34:58 GMT  
		Size: 2.4 MB (2377827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f21fe89de22cc5a1a591e5a49f02eee67a996e665cf639549ef14cd119afbf9`  
		Last Modified: Tue, 17 Feb 2026 20:34:57 GMT  
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
