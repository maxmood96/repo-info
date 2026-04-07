## `sapmachine:17-jre`

```console
$ docker pull sapmachine@sha256:92b9b87a5d28d3d757933a5a46b0095f761f0c9873fddcb25f4bf3192405aaa0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre` - linux; amd64

```console
$ docker pull sapmachine@sha256:04e29e7d38a88ff640640db77538ca6eb4a405197561edb3023b0dddea2e7521
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84504118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d536ad55cc9db7ad4b91e3498a3c20a21d13fc898de9c04cdf7b6696e0911e52`
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
# Tue, 07 Apr 2026 02:33:44 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:33:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 07 Apr 2026 02:33:44 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30eb02bd9f4bd036c2dfd337ed0b0627531676c80ba2a9a4eba9d0d538f2709`  
		Last Modified: Tue, 07 Apr 2026 02:33:57 GMT  
		Size: 54.8 MB (54770659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b988951557839a83cbfea254d1af4bab3e43e856a91c4da713d4537e8681cb1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2529848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06c2faa2eab0d75f07250cf1238ef461f3b3b87c42423db0aee234b8b0874e26`

```dockerfile
```

-	Layers:
	-	`sha256:25f71d93f4fb5d8148999f1bcb8eb36339e3c7c38762d769bd974fcf94a33dee`  
		Last Modified: Tue, 07 Apr 2026 02:33:56 GMT  
		Size: 2.5 MB (2519802 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6639ba3b5710b6e8d49382288f7f0ca5fdc1be487216d8ea738061b078ab3cb`  
		Last Modified: Tue, 07 Apr 2026 02:33:55 GMT  
		Size: 10.0 KB (10046 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:db0dc22e3e436431e969e89087859e1f2ac08e3b7f7316f0895a112af6b517f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83076480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6445d5b6a40f612b94feabd66d724d46eef57ddd2f7cedf112455258d70a1e2`
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
# Tue, 07 Apr 2026 02:39:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:39:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 07 Apr 2026 02:39:47 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02eaeded2cb38350ca967c2ef8c9b0b2f274b6cc3940718b91ff86fb9bf07ba7`  
		Last Modified: Tue, 07 Apr 2026 02:40:01 GMT  
		Size: 54.2 MB (54202405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3b61c8478ec5d09948c918f7fc9d63fa294b6bd0888f82bf1fcced70a9164af4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2530515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22c1c2e7a09c4fc3e537aa647ca4e3f55a4b4b25aa818d4a18ee59e0b02b32c0`

```dockerfile
```

-	Layers:
	-	`sha256:5d11edc72593e02dc66f09a6226b82972df837cce92514ff7c0848b6bdc7ba72`  
		Last Modified: Tue, 07 Apr 2026 02:39:59 GMT  
		Size: 2.5 MB (2520318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efb0c966f4a098caf1cc2cca507288af3ceca8a7f45e5a086f6a6628cec2b466`  
		Last Modified: Tue, 07 Apr 2026 02:39:59 GMT  
		Size: 10.2 KB (10197 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:e71d0d3d76d86bd0269eda6185466e27f0d7029ef92b74c03fa8bac1e0073e33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.4 MB (90356393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5407fe128fc92c2679936bdafe627c0355628a294a061077153f2aad400cb83`
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
# Tue, 07 Apr 2026 09:11:30 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 09:11:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 07 Apr 2026 09:11:30 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2206a81f65df3147f8c62d4c01c47495515dae16f93ce6845cd7cdacdd206f1e`  
		Last Modified: Fri, 03 Apr 2026 15:56:51 GMT  
		Size: 34.3 MB (34313334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37c39d59f5a5635c5765b7026763eb8f2645bcee117321f66fddd228aeb0fc5`  
		Last Modified: Tue, 07 Apr 2026 09:12:05 GMT  
		Size: 56.0 MB (56043059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e6028c749b2ad3a463705f8463fda460e84e48209101e515c21b92568c17bbb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2529414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6115c9d9bd5260b788f7759256a0b91dd1981a0dc7a4f1ee2f4808450297d92a`

```dockerfile
```

-	Layers:
	-	`sha256:480954c9d26bbd1817dd16b8271ec28a97aca56089c3ecf107f7e71740ec13b0`  
		Last Modified: Tue, 07 Apr 2026 09:12:04 GMT  
		Size: 2.5 MB (2519300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b20c335b0057239b1eb597d79645d26eb95dc6af85bea5bb6786444ea16cc6b`  
		Last Modified: Tue, 07 Apr 2026 09:12:03 GMT  
		Size: 10.1 KB (10114 bytes)  
		MIME: application/vnd.in-toto+json
