## `sapmachine:lts-jre-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:c9d423f716d103dcc7e54d075fb7e5e3fcf95bbd7a7afa6480d0db8c936a08f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:904fbd8c366a15b0e74536a28ea3fd0432e5d1ad1b2514c9b8e0467545f69b09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88683049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ba458cebe56b9703907504115fc2fc0ee6ac53764b5a7b4dd89eba2fa8ffa5`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5930f1e1aac88121a9204f83d47c14ae98dd63d6c58d3f08a368f82357523a18`  
		Last Modified: Tue, 04 Feb 2025 04:48:53 GMT  
		Size: 58.9 MB (58928759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:08af42bce41af038fcc120ad1ca9fe3dfb22e7c9024dff2b03c587ef1b603307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2163853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a577d5fd4842f9883208c0e058885cdb67bfc9981381125558ce1fcebac23244`

```dockerfile
```

-	Layers:
	-	`sha256:e08a333e05afbc49115f0ea23a084644de83056952f6a9f002a47c35b3c2ef3b`  
		Last Modified: Tue, 04 Feb 2025 04:48:52 GMT  
		Size: 2.2 MB (2153203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3937c35efdad7e99f90b29c093baaac4a3393664826c10b7cfe8201036281653`  
		Last Modified: Tue, 04 Feb 2025 04:48:52 GMT  
		Size: 10.7 KB (10650 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:a530bea7718fc8e0b72debbf87451d0efd29bda75c518e20036d2cfcaaefc31d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (87000286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf2c1b919fec4703c16847b4546d19a534cd980999b3dc1621c481178163eeeb`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:45 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:47 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Tue, 19 Nov 2024 16:18:47 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fac9b41159e950b31a13d8ab2b83639bc7dc9dee9c455d1ceb996b3078e25cf`  
		Last Modified: Tue, 28 Jan 2025 02:37:52 GMT  
		Size: 58.1 MB (58107615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7762a89c2f542c65647de9b90533c773978a14eb257c379c4054836a3bffc8e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2160573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e8d9e1c8737136408fc0b352335d7a999ea772908ce261f0c4c534059ea0c32`

```dockerfile
```

-	Layers:
	-	`sha256:0bc453b1219fc2f03120aef2a733852d6b6b9083e153ff2bd79718363ef9d6bf`  
		Last Modified: Tue, 28 Jan 2025 02:37:51 GMT  
		Size: 2.1 MB (2149760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1a0503f2705a5af2c1b4947364c5ae74a49b579afb4f5f89b84bb53b2b2348c`  
		Last Modified: Tue, 28 Jan 2025 02:37:51 GMT  
		Size: 10.8 KB (10813 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:6f978ad44907175ba8a6a1b5d2f3de08860721aca69065927ecbdc2124ffb408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94823417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5c1398a6a1d6f658bec356a75023215d50a1298471aa04d357a8b6ef6cee562`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:47 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:50 GMT
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
# Tue, 19 Nov 2024 16:18:50 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdecfdb7a232e086365af9f15b64ad258db901bb96d0800105df7e114e283777`  
		Last Modified: Tue, 28 Jan 2025 05:49:03 GMT  
		Size: 60.4 MB (60434597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:bfb7b7e4977226d448147d3c7fe5677cae113f02ea6ee3b442917ec50915f9ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2163872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7b9dc696d8187f779da185057cc55265baebbf3ce09d4e6f30fd7d8f3c5afc2`

```dockerfile
```

-	Layers:
	-	`sha256:6d618484c31046e12618d25346500fabf33642ef958b563184f457a9b9e58250`  
		Last Modified: Tue, 28 Jan 2025 05:49:02 GMT  
		Size: 2.2 MB (2153147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7b7c73483eaec4fb3e4f41dcd897a9e4cab8be9b14dc49d4c4d1853f1501435`  
		Last Modified: Tue, 28 Jan 2025 05:49:01 GMT  
		Size: 10.7 KB (10725 bytes)  
		MIME: application/vnd.in-toto+json
