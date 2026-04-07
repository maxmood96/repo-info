## `sapmachine:21-jre`

```console
$ docker pull sapmachine@sha256:632acd4e805787cbf13c6ec16aa8c94f6274435d8fe9239541210376b41fb9e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre` - linux; amd64

```console
$ docker pull sapmachine@sha256:6738342a2910962f65e14e34acf85de0003f6e9f808ab9ad9cce438fe5025ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.5 MB (90476022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63d86a619078dda53ba138450fe68dfed297f6329e643b962d8f2145bd55d713`
-	Default Command: `["bash"]`

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
# Tue, 07 Apr 2026 02:33:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:33:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 07 Apr 2026 02:33:16 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf5c63b95ec1171b54c8cacd8b2e2901e478598a5a09f3d289e2258eb6508cd`  
		Last Modified: Tue, 07 Apr 2026 02:33:30 GMT  
		Size: 60.7 MB (60742563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5a2e36ac71ad941aada58c3086b240a7814949234cfe91b4c9c04ac35017f93f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2531193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:093dade5aff5c07af5310aac6268266e5937f75e96986b01d7780d1f6d48694c`

```dockerfile
```

-	Layers:
	-	`sha256:34398e9363159e677c676040c42fc842c2afa6607d535db4f110e770e731635a`  
		Last Modified: Tue, 07 Apr 2026 02:33:28 GMT  
		Size: 2.5 MB (2521108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75e8d3c29e057216e2326e4a1f46f8173f71e4bef4a8e33ef5dd313b4440bb12`  
		Last Modified: Tue, 07 Apr 2026 02:33:29 GMT  
		Size: 10.1 KB (10085 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:010d03877c5b1026216e465221d6e5cc81fd0849f2a44eaca9300ee5cd5126fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.8 MB (88808017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10d97b0530b2c2f1b3c6b84c6af3ea60f64d19555560d7d24417f84133b1aa33`
-	Default Command: `["bash"]`

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
# Tue, 07 Apr 2026 02:39:25 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:39:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 07 Apr 2026 02:39:25 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3427c7e97da0601c3d31b147535bc949e9a7c0e1708a65367ea1c903ea19db4c`  
		Last Modified: Tue, 07 Apr 2026 02:39:40 GMT  
		Size: 59.9 MB (59933942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ebffd418d4b2648b4191a1e6b33694ac4f1074030050ebc057f2a5c93dd89014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2531862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33b7889e784ee3a95da8bfa0d24def789a16877e582e8f04be29e6571ed106f4`

```dockerfile
```

-	Layers:
	-	`sha256:24d7dcf495e0ff1707c13eef1aaedcf7de07d33e8b4aaf2bcaea9581d002c41e`  
		Last Modified: Tue, 07 Apr 2026 02:39:38 GMT  
		Size: 2.5 MB (2521624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:471dd7eff460ae64c2825e1ebb80d31b4e90c970df6c6c09bcf6f1e9d8e20a0a`  
		Last Modified: Tue, 07 Apr 2026 02:39:38 GMT  
		Size: 10.2 KB (10238 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:371e3d8214de6880e819ebc464f9c0f4dee0dfcadb89fcf0dc6d3aa6e12e6e8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 MB (96359809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70406883ad0cd0009ae077796bfca9d788bd1e493d1ba7a6e1ec4fb9b54a4c6a`
-	Default Command: `["bash"]`

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
# Tue, 07 Apr 2026 09:07:59 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 09:07:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 07 Apr 2026 09:07:59 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2206a81f65df3147f8c62d4c01c47495515dae16f93ce6845cd7cdacdd206f1e`  
		Last Modified: Fri, 03 Apr 2026 15:56:51 GMT  
		Size: 34.3 MB (34313334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191548f38f7dd9b10bd6d54674be16e183e8c14352c16d135ad974992d3453df`  
		Last Modified: Tue, 07 Apr 2026 09:08:25 GMT  
		Size: 62.0 MB (62046475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre` - unknown; unknown

```console
$ docker pull sapmachine@sha256:bca8b73bd5656973aa5b080edc9cf74484c75dd1ea6c83328eae4f1c30561ea6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2530759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55f45ae2b1dd5117e3ecf12afdc6a99359b8948d85b9bf266696c85f806b6720`

```dockerfile
```

-	Layers:
	-	`sha256:ba2ab9d9d4b7ce869f7865220be6624f0cf62b2d81395094cb46882bfdb6e1ce`  
		Last Modified: Tue, 07 Apr 2026 09:08:23 GMT  
		Size: 2.5 MB (2520606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d47c2859b5e3526f0d955c3b9464280bd5c13f4bd38ef08f14ca39c0fcac8656`  
		Last Modified: Tue, 07 Apr 2026 09:08:23 GMT  
		Size: 10.2 KB (10153 bytes)  
		MIME: application/vnd.in-toto+json
