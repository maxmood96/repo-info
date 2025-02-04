## `sapmachine:21-jre-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:75bbd930fa14673bf25964476b8273ebacef19ea4c7a49abd80ca903d6b83fa1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-headless-ubuntu-noble` - linux; amd64

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

### `sapmachine:21-jre-headless-ubuntu-noble` - unknown; unknown

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

### `sapmachine:21-jre-headless-ubuntu-noble` - linux; arm64 variant v8

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

### `sapmachine:21-jre-headless-ubuntu-noble` - unknown; unknown

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

### `sapmachine:21-jre-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:32ed1e1c414744fab5b1af30c8d602514750679b7a81c0213d6828e8763c3816
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94812651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0149e75369f0e5882266e1ff2a9aecf2257e46d4acb5da7d03537c7f53662395`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:16:03 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:16:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:16:07 GMT
ADD file:8c71b040cc97f9d076a34d57cd957e6b33cdfb8f115e1ba283b674e6aad793d8 in / 
# Mon, 27 Jan 2025 04:16:07 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Mon, 27 Jan 2025 05:10:08 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:979a978d025388fdcb9cead9f72de81d25d71156ad8b1f89702acb37a96f6422`  
		Last Modified: Tue, 04 Feb 2025 14:39:15 GMT  
		Size: 60.4 MB (60422827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9026c394aa0ef09da226582a6f015cc05347967b6307894ed1426dbf99ad8938
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2167834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddf52aa8d5520f422ada77b7e0aa9ea3f83d43eeaf645b269fbfa42d99a82bc5`

```dockerfile
```

-	Layers:
	-	`sha256:886c84b43e3f8c8d5c78c51278ae0725f8be87c18865e19c826a24c50c1798f8`  
		Last Modified: Tue, 04 Feb 2025 14:39:13 GMT  
		Size: 2.2 MB (2157109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c95428b2c03c44f6af2b599cef718be52a685c2cfdf5b0ec0d64053afebaabf`  
		Last Modified: Tue, 04 Feb 2025 14:39:13 GMT  
		Size: 10.7 KB (10725 bytes)  
		MIME: application/vnd.in-toto+json
