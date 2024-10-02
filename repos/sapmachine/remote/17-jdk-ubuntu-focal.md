## `sapmachine:17-jdk-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:24da6b7c44d96ca96569de7d20e86c23a568f9ae82c32de6475fde9f0ec02bf2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:eb47ee684d0c27535d8fe6182b9b64f1345c78add248bb940151a0565ee18c61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.1 MB (227109119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:105dade81fe66a411bad26d52d3590f1757b9c7d78dedc95744aa5d61dee1ee5`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3823320faa42774534fd7eee0bd245af8cec6a720ad722144d40efa229291d8f`  
		Last Modified: Wed, 18 Sep 2024 05:32:37 GMT  
		Size: 27.5 MB (27511052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e99640e4f2e26126e3506ccb496ac06ca8f4d38bae7b94ba6885d5505dedf1e`  
		Last Modified: Wed, 02 Oct 2024 02:00:11 GMT  
		Size: 199.6 MB (199598067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3eda1a896b213fde24bb69ba8881db9d5f2454fb4ad50a74565636067ec2cfd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2373898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f7126629fff6048c3cc17abdf31ab73c1dcb0917643dc49480056d4ef5826c`

```dockerfile
```

-	Layers:
	-	`sha256:d6027e05062b2362e53ba1844de2f5d2fe9b753d4245b8280a7ecca82f7767f3`  
		Last Modified: Wed, 02 Oct 2024 02:00:09 GMT  
		Size: 2.4 MB (2364009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ea0463e5ea97fad5073bb1a98f5a08b218f5f693d1ec3f1d29865a7c06a3123`  
		Last Modified: Wed, 02 Oct 2024 02:00:09 GMT  
		Size: 9.9 KB (9889 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:444b2edad35caaabf708001085c8fa19d7663e6900b4b58c73929ce6d1d067a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.2 MB (224193233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58c8c9f0368c92ec9398b0aec60cdbd7954997ec7f76cb952e80971a5229bd2e`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f7087ec3f63a82386ce40d74d075d761ece5bfaefdc30b9ef62f73ecfb2e41fe`  
		Last Modified: Wed, 18 Sep 2024 05:32:46 GMT  
		Size: 26.0 MB (25973592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8369cca2103d72509b3de486f8d89e9f660484fb1b9fb139aeb47eee7dc945`  
		Last Modified: Wed, 02 Oct 2024 04:00:51 GMT  
		Size: 198.2 MB (198219641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5c58b9680f546dd0248b53d93836289b3af7b202d3d518574abba60e23ea77b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2373728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e4250649c101fe632c0f54bfe635ad41388f6d749fcf768aca9d8362bb3435f`

```dockerfile
```

-	Layers:
	-	`sha256:760f8987a958e38a149cd3335e88f3d9788877aa6ead7b4ef9ae1d60d6942bc5`  
		Last Modified: Wed, 02 Oct 2024 04:00:46 GMT  
		Size: 2.4 MB (2363693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27cfb0b7bcd4a8e492623a8907f3637400d3f31ae708db55430d19d3366db534`  
		Last Modified: Wed, 02 Oct 2024 04:00:46 GMT  
		Size: 10.0 KB (10035 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:34f1c5cc8b963008d80e31b680645457a1e9870af3e11a7623acdf579b360fbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232362993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c86d48f8c43d4075a4c2ec2e5f0d06a3448019c7e7aca04b8a2d5eff301222`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:c6515e5ea6494efa348e1177d50c0c28bb8236a5d2b518388f13b7d5a528d4fd in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cafd57629abc05d597016161b87b83b544a17d39d1016cfb289a60295fc7d492`  
		Last Modified: Wed, 18 Sep 2024 05:32:58 GMT  
		Size: 32.1 MB (32076334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac013c3833ab81b491475f5f4d4458dd232805627382eea32001924f7fd57e2`  
		Last Modified: Wed, 02 Oct 2024 03:15:35 GMT  
		Size: 200.3 MB (200286659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d5b234b2424dd2e48bb0f97d40932e38f598c08b1bae45f8ea3b0036df69fd91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2375800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4574845ffb27fc47ddf69997418248d806464e20e92a686fa0a232832ce49e3`

```dockerfile
```

-	Layers:
	-	`sha256:fc8773fa773cc424932e8e4a4cb5aa52a04d43abce41f58768860895a6b71f38`  
		Last Modified: Wed, 02 Oct 2024 03:15:30 GMT  
		Size: 2.4 MB (2365849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36b76b2e071ca1a9a35128092a8726ab0fcead22611c2539657925e7ddb9b661`  
		Last Modified: Wed, 02 Oct 2024 03:15:29 GMT  
		Size: 10.0 KB (9951 bytes)  
		MIME: application/vnd.in-toto+json
