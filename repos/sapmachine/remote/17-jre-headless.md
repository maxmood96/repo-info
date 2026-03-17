## `sapmachine:17-jre-headless`

```console
$ docker pull sapmachine@sha256:edd48c9dab47d892be923e56cef102f7146fdea9f206eb56f16d18a9a942ea9b
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
$ docker pull sapmachine@sha256:536816cdfc72cc796c8b9e6e6a49748937bce76b97e48f5e27545b0dd04232b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83319904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5b2b6396b825f083371080e73ffb3bb4eeeca2b3ad55dc479a2a1ba6989d01a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:25:09 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:25:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 17 Mar 2026 02:25:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:268bf8fc00efddbfebac3e55bc73cd3e9b54b948d8e1768879d59a1fff2e0f59`  
		Last Modified: Tue, 17 Mar 2026 02:25:22 GMT  
		Size: 53.6 MB (53587911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless` - unknown; unknown

```console
$ docker pull sapmachine@sha256:855899cf2d800e3611f67186146420b5db89459c44defcd907934b0fc2231120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2284209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17e5844a3b5fd5a4bc181b5345e50543af326c868307a7d934a64ca5037a4d78`

```dockerfile
```

-	Layers:
	-	`sha256:1d82a76481992aa6ed911343f6f50f757c8eebdc67baaa41908975fd12e191ca`  
		Last Modified: Tue, 17 Mar 2026 02:25:20 GMT  
		Size: 2.3 MB (2273980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39e85d1c894990fc12333a201a08324344ec78c05ee9680c1e37b38f12a565af`  
		Last Modified: Tue, 17 Mar 2026 02:25:20 GMT  
		Size: 10.2 KB (10229 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:60eb67999d11c33d4459bfd54cd0405a9bbd74070c418f1cb0c32f83d0b008c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81878808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a517c8f6c661312550901116afd295d4716388db3742426c2f28bbc18af7ef43`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:31:26 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:31:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 17 Mar 2026 02:31:26 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3107c18f8b1b5683afb8fb390658c051936d56ad2017bc6f5cd586b976a6c7a`  
		Last Modified: Tue, 17 Mar 2026 02:31:39 GMT  
		Size: 53.0 MB (53009099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2ba7bec556f26f93ea3762693f04730ea11755af344556aa218cce15bc1fae15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2284868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:445310fd93a2c0f2dab0930e6a24fc4ff85033eae68c66dd387a6e72bc67c2ef`

```dockerfile
```

-	Layers:
	-	`sha256:7a2abe23cad8dd03c62537195dc14f1018216b501870e30fdcbc48d264dad651`  
		Last Modified: Tue, 17 Mar 2026 02:31:37 GMT  
		Size: 2.3 MB (2274487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f6ac8638de0a45cbfb5fddac20388c8fd7984488b4bbecdb8c4c0275dd90fc3`  
		Last Modified: Tue, 17 Mar 2026 02:31:37 GMT  
		Size: 10.4 KB (10381 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:b64d121ddc785990fa185bd0b149a11adb8abc6ee488e209a1c6bf89b7296887
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.0 MB (88973722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:570612b96aa3e3f490e26abc21816be27eee4269ad32fc5abaefdb13325e5dfb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 17:18:33 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:18:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:18:36 GMT
ADD file:2a89eb67bf550d9680999e3ff99dbaa17c251b6c343a241318e879a26da53fca in / 
# Mon, 23 Feb 2026 17:18:37 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 09:51:45 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 09:51:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 17 Mar 2026 09:51:45 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f826c9b754a00ada9d9335ffdf3ffd40f6925a3223caac76cc429823b8621f9e`  
		Last Modified: Mon, 23 Feb 2026 17:51:39 GMT  
		Size: 34.3 MB (34310051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7759c2fe94f1b6417d95f41b571043f470cf03bd754a03a81a55382c96be6f`  
		Last Modified: Tue, 17 Mar 2026 09:52:14 GMT  
		Size: 54.7 MB (54663671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless` - unknown; unknown

```console
$ docker pull sapmachine@sha256:35faeb1604822c19413e14255478587063b70ba4c9d0ce52e7098d844bb79204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c7ae063283e430d36f50d6c79ab4d84c8e2dcf73a6e6ad89383d63018bb4b90`

```dockerfile
```

-	Layers:
	-	`sha256:aa136ba4878270bd437839d520c9d25f09d93a3d1f577b2ee75da1f22f4ccf4d`  
		Last Modified: Tue, 17 Mar 2026 09:52:12 GMT  
		Size: 2.3 MB (2273397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3bb75f10e586ef9f5c1e7d1b5599e615d52d5511cb402e43e11d2c219bdde14`  
		Last Modified: Tue, 17 Mar 2026 09:52:12 GMT  
		Size: 10.3 KB (10296 bytes)  
		MIME: application/vnd.in-toto+json
