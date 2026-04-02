## `sapmachine:21-jdk-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:42c44db3c73bb08818f4953f69d4274aa1bb43de195eee736d576479065f672d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:f2208737ea008fa78b41db3401d993848ba8d5c04754b45811272e564622fbf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.8 MB (245845801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94c952646e40ae15681c867ca60bb685c6ec22e4935880309d11f73cdec25e38`
-	Default Command: `["jshell"]`

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
# Wed, 01 Apr 2026 20:16:55 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:16:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 01 Apr 2026 20:16:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1415fe3a3977fdf4b98359221a09ac46a0cd11522c63ba344b69b00516986b7`  
		Last Modified: Wed, 01 Apr 2026 20:17:18 GMT  
		Size: 216.1 MB (216109388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4f22fd3bae81ac1e09747bf8bfced1276c03b8b2473b53de597533525fa792df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2642305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d25943baa93554e6d9b76772c1c3997a613c030499f02adcda47f5159ebda08`

```dockerfile
```

-	Layers:
	-	`sha256:6a52e5e47273d46c2003b9697ee08fd071dd05266147846dbafa32bd7a751cc0`  
		Last Modified: Wed, 01 Apr 2026 20:17:14 GMT  
		Size: 2.6 MB (2632170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04844bc0a7ede3aee01cdb483252c61c4b61b016ed1e1d81d7e848c3fe6e29e3`  
		Last Modified: Wed, 01 Apr 2026 20:17:13 GMT  
		Size: 10.1 KB (10135 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:81ab354dab11ec02b3277e3fd6c50bbcece4ecb8e3ee416a43a693487ccbfd1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.9 MB (241929496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb7a9171aaf8db9afcf08ce46d5723a3f414a60510d7eda34c3acf5f581b2075`
-	Default Command: `["jshell"]`

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
# Wed, 01 Apr 2026 20:16:31 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:16:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 01 Apr 2026 20:16:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3cd02cf3cf3dae590223dad36725ad521d3c27375424e9fc0b95f64e9f626ba`  
		Last Modified: Wed, 01 Apr 2026 20:16:54 GMT  
		Size: 214.3 MB (214322553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ab1fbe5ffbea47ab0322323587f4813f892ed15299db9f23affe0df277d7d215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2642187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df6858dae511824c9a23b271018a59ed1b0892768b31323c41927b6dd0a92e6e`

```dockerfile
```

-	Layers:
	-	`sha256:de3cc9c31fe8c7ba4a3b67bcbb048b555e9a113a4f2b2ce58e0f96d508ba6861`  
		Last Modified: Wed, 01 Apr 2026 20:16:50 GMT  
		Size: 2.6 MB (2631900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:975730fc5923c8b9547dd529554e487549de689e39f221c76aa771b4423072dc`  
		Last Modified: Wed, 01 Apr 2026 20:16:50 GMT  
		Size: 10.3 KB (10287 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:56122624a44e9721a6361bb0ef686168591520dbd2d4deabdce1514d68c8395f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.7 MB (251723206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:410241c89d38ebb0bd5dcad37256d9223db1c705d07a15fc635cdd66a9c0ed80`
-	Default Command: `["jshell"]`

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
# Wed, 01 Apr 2026 20:47:26 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:47:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 01 Apr 2026 20:47:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6fb1b04a0a70d070de8a04181c7b855a46b1ea4f771660ae7f0783acd4569be2`  
		Last Modified: Sun, 22 Mar 2026 18:43:46 GMT  
		Size: 34.6 MB (34649660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e298b26a53dc91dd4f0e4fa30ca9482d526fa72e8661fcd635426355b63b31`  
		Last Modified: Wed, 01 Apr 2026 20:48:15 GMT  
		Size: 217.1 MB (217073546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7f5a5c72182c4d8117ddb1cac1f96d54818e27f500a16cb60689e499d89ac985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2639983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78be4cbd73b38174110c8806bb7a3a4060212484339e5056d0c3e8fcfb2d76ef`

```dockerfile
```

-	Layers:
	-	`sha256:1d89e7787fff2eb38573199de1114aee3f8ca27b6551583f5b22369692f15eaa`  
		Last Modified: Wed, 01 Apr 2026 20:48:06 GMT  
		Size: 2.6 MB (2629780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9092c9494f6db4a2d7240a5416d3d9726f614bc34b3e8d12903b0a045cec0627`  
		Last Modified: Wed, 01 Apr 2026 20:48:06 GMT  
		Size: 10.2 KB (10203 bytes)  
		MIME: application/vnd.in-toto+json
