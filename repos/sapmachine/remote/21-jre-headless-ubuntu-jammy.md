## `sapmachine:21-jre-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:c9b4b98adbd0ae138f830c8ee77306a3744dd6ec8c70a56cff2626c085dd7b42
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:dbd8a3c96648e52c8ec79f9561549bb51678d4786ff89eb94e935aba7480978c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.9 MB (88863394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92662db16a70319e3ba68bfa711c2112c0c622181be9529f7e4e6980c9ab8e79`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:16:43 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:16:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 01 Apr 2026 20:16:43 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d548c6a3c6fb2bcc7d047ca6bacd2f451af35da1ca8f04dce3d6f540afa134`  
		Last Modified: Wed, 01 Apr 2026 20:16:57 GMT  
		Size: 59.1 MB (59126981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7ef071466e9030e3386c8f93fc0d4363e88ef011866c5b5fefc1ef9e71e1daf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f473c95b04d41edf5fb4d891c310d3c4c6a4c09224d3ac3de9ec9bd41f5f0e95`

```dockerfile
```

-	Layers:
	-	`sha256:8a671645a4346dcec7de97f4e70b5a1adb1f08b730e7d9429c44d111bfc7611f`  
		Last Modified: Wed, 01 Apr 2026 20:16:54 GMT  
		Size: 2.3 MB (2296537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:529f4f393f6c9958cb657615ba5b76541d487361b892cef869a83543c9971452`  
		Last Modified: Wed, 01 Apr 2026 20:16:54 GMT  
		Size: 8.9 KB (8909 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:cb0f7000e190cee81276c9323d5322f713096948ff0161b40dbcd5c42a59f94d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.9 MB (85889291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:211e406e021b98da435109950ad1e99afa983192ea75d4d0b9f619ed4557ce3c`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:16:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:16:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 01 Apr 2026 20:16:22 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125554f9d887cfb2e868480f9e4bcbab8d8d50e3f55068bbeef170e6bd376ad3`  
		Last Modified: Wed, 01 Apr 2026 20:16:36 GMT  
		Size: 58.3 MB (58282348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ca1a720622f2a56ee3ac6aee638cac06cbb285496d696c8e93dd366e356544c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b2d260280792ffa06c0884c0674a573de430fc3862b208c6a7e5414714ddf46`

```dockerfile
```

-	Layers:
	-	`sha256:f56f4eafa207f67809d58e76ed026b614386a9edd11080919916738cc3c8d81b`  
		Last Modified: Wed, 01 Apr 2026 20:16:34 GMT  
		Size: 2.3 MB (2296209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b1119fdffcb748fae69afcd99244c18be555b7fab8c106e643cb8590685ef49`  
		Last Modified: Wed, 01 Apr 2026 20:16:34 GMT  
		Size: 9.0 KB (9013 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:c71edf26c6e42fb89677f6d64d411d105b69a6e3285d5509c3887c3d3b6a0df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94829984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:326c60456f5ea7c2ebc484f94d48e16719b9aa667659e80ce114ed8cc45b62cd`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:11:34 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:11:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:11:34 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:11:37 GMT
ADD file:268be611d24f69c3d8e480314cd587652e4c89a6032236737057c8b64f2379da in / 
# Sun, 22 Mar 2026 18:11:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:50:19 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:50:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 01 Apr 2026 20:50:19 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6fb1b04a0a70d070de8a04181c7b855a46b1ea4f771660ae7f0783acd4569be2`  
		Last Modified: Sun, 22 Mar 2026 18:43:46 GMT  
		Size: 34.6 MB (34649660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ac7db31a74a009e81c8bdc97cebc12a7f4124ec9a1845f4231cdf0e686c199`  
		Last Modified: Wed, 01 Apr 2026 20:50:45 GMT  
		Size: 60.2 MB (60180324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:aa0fc338a70a7f853e29e79575b57c766af5cb39af0ef2de5ccb9efe2afb4df2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fce9cbe90056695e0ad1802151147fa9f62aba8eec6f7bba743999d0fbd842aa`

```dockerfile
```

-	Layers:
	-	`sha256:3d92f84552a160f3b3833766a249548512b19c877590b7ad808abff8c81d34f9`  
		Last Modified: Wed, 01 Apr 2026 20:50:43 GMT  
		Size: 2.3 MB (2295979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb53b11a5f7db2159b9cc6a5d0d6f1cc9c8dfd1a922955fcfc4b6c8f92c4c0ec`  
		Last Modified: Wed, 01 Apr 2026 20:50:43 GMT  
		Size: 9.0 KB (8953 bytes)  
		MIME: application/vnd.in-toto+json
