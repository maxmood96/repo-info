## `sapmachine:17-jdk-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:c28e3ec78ee1bc57c75ecc1f88c333459856e4df3b966bb0f642a5e89cd9c6b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:4979ce5fbc7332a3794bd073376e957a6be3e1fd95ee30534b1366667e87fdb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.8 MB (230835586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52e5b63dc4aac0e87c02ea314c2243485aa7b6d7ec6d4d9d69e94d25a9ab024d`
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
# Tue, 17 Feb 2026 20:35:36 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:35:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 17 Feb 2026 20:35:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0ad044f0c4ddcb30a4fcc7cfe84da95e34700e95572bef00f3c5623938959c`  
		Last Modified: Tue, 17 Feb 2026 20:35:59 GMT  
		Size: 201.3 MB (201298220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:53d9e8d777d874b491126a3e9f69bef157a10d0a0e1bce77455ceab7e3c4e0b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2640345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43d45556f434a56ac6679470a7ca2a234c7f8dd8f9b85fbcd7d5806d01add11c`

```dockerfile
```

-	Layers:
	-	`sha256:cbd9ef511b51b08bec6f671b29b4fa01cc8c83a266524c6b7a5622606ac956a1`  
		Last Modified: Tue, 17 Feb 2026 20:35:54 GMT  
		Size: 2.6 MB (2630251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:198c88f4640a58a0d81172efb8ad0b15f2f94969d6a544fae0dcf1ffec5b21bf`  
		Last Modified: Tue, 17 Feb 2026 20:35:54 GMT  
		Size: 10.1 KB (10094 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:9d19b391573ead81a11231988297a7f54cbf639601e33c927613b0461cf19ac8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.4 MB (227363234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:698908d9a439302dde6dee43c298aac97b3fa3d3f8d09f125225c857ed0741af`
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
# Tue, 17 Feb 2026 20:34:32 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:34:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 17 Feb 2026 20:34:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2eb228e2c8df9fc9838ee73e867233d14ecdcd33db157bce4fdbd4bb6a507cd`  
		Last Modified: Tue, 17 Feb 2026 20:34:54 GMT  
		Size: 200.0 MB (199978290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5099f1bbafd7fe4d7af959fbfca598d5df7a9d1ccdae34a662f7bfc1b5529f76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2640228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5513fdf15548b2e9e54ad60881e67ffa0255ec3a3e60e1db50962f3ef43a4be2`

```dockerfile
```

-	Layers:
	-	`sha256:0ac04f5c6f7b3bb840d1e4adfa248bb7a169f7b0aadc3f9ee7be1e6c62fa5ee1`  
		Last Modified: Tue, 17 Feb 2026 20:34:50 GMT  
		Size: 2.6 MB (2629981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c3661920433e3258ffe4cb2dbd8686278c2049c185cb8fd759b4000e46363b1`  
		Last Modified: Tue, 17 Feb 2026 20:34:49 GMT  
		Size: 10.2 KB (10247 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:d7b2a23f1affc13ea064f0b229c585473fc46bc68ab210b59c1b46fc79298ebb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.5 MB (236511490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2adad927e92e19256dfc6095beb65b0f1a4b7c51cb188b8bee7d52526c2818b7`
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
# Tue, 17 Feb 2026 21:38:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:38:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 17 Feb 2026 21:38:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:95401e425d899946469007a0ce4b02622cf84a67cdd684aa25d61d472fffc38f`  
		Last Modified: Tue, 10 Feb 2026 18:13:52 GMT  
		Size: 34.4 MB (34446102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93a0e20af66defcea2f9f34ef9d06995e8d6cd860288d784a48b1290cf2f707`  
		Last Modified: Tue, 17 Feb 2026 21:39:33 GMT  
		Size: 202.1 MB (202065388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:cb1a7d6387d4b0a7de04fb493a9c76419c7d937b1679c5b26b8057d4e4bc9620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2638024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41d0e130f805a81ad4610273bf6cbc4d9e3efee70c48d415cc65ea1edf8aeaf`

```dockerfile
```

-	Layers:
	-	`sha256:e5c336a3a47412c12634944e526203a175dd81bd41ab2607c08ac62bf144e415`  
		Last Modified: Tue, 17 Feb 2026 21:39:29 GMT  
		Size: 2.6 MB (2627861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d627cb6060c2f2980b9cfb604445a2a2a90064d3be9f0ce95b1dfc2cbd2466ab`  
		Last Modified: Tue, 17 Feb 2026 21:39:28 GMT  
		Size: 10.2 KB (10163 bytes)  
		MIME: application/vnd.in-toto+json
