## `sapmachine:lts-jre-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:947d8c9ddfbf473ae86d456a6c97d9e7a55c923e23ba9dca73fffcd423804a52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:012827e886d63dc4a30402b9b69ffafd246b76bf156d5c5de4505e05860f2463
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87463979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ae41908fbddd73a21e0a732183125a67d1222c99ced4a5f66cdaab9a15a49e9`
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
# Tue, 07 Apr 2026 02:32:49 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:32:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 07 Apr 2026 02:32:49 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed4c3395a878313cc790c56a79446a4ae3061bafd2916b18f62cd2dfef52dc9`  
		Last Modified: Tue, 07 Apr 2026 02:33:03 GMT  
		Size: 57.7 MB (57730520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c1486e3d69b1c32fed1f34149cf146a987238575a22baf7c80d7e8eb3df99825
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2538198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fbc5d87e0dd1723350464e526126a4c2bde7c23daa47b488e46eeeffd0655c0`

```dockerfile
```

-	Layers:
	-	`sha256:a3a5930ef423e8a56f20893a13ead079b8f286a9ab90134d6d40265e0601e19a`  
		Last Modified: Tue, 07 Apr 2026 02:33:02 GMT  
		Size: 2.5 MB (2527174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1938284a1500f7d0cbacc7445cf53a7937db776a54ccb6addd3bad7fb8f2e027`  
		Last Modified: Tue, 07 Apr 2026 02:33:01 GMT  
		Size: 11.0 KB (11024 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:4191c6f45699fc0c843e6c52e0e713dc14721363367ad997b5d045743b5588ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.6 MB (85576416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd5f5ccd4279d59302aed8a2eb48f35441b3fcd2e1dea03d8a9cd5024e936a03`
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
# Tue, 07 Apr 2026 02:39:02 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:39:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 07 Apr 2026 02:39:02 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beba1748242abc01b94d811619eb8d124119efddd9221a126b719a9173336750`  
		Last Modified: Tue, 07 Apr 2026 02:39:16 GMT  
		Size: 56.7 MB (56702341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:90009e7bdf0b9d46acc02ee8fa015d5d3f1ae5f685d4cd141294792daecd1af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2538938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e206d1277657c22d66ab4f1239a9c2a02a08145026fea26c0fd518d2a1eb70c2`

```dockerfile
```

-	Layers:
	-	`sha256:c97db6ef016503052d225b1f8b199f545e44207a72c66038df08f11370a367cc`  
		Last Modified: Tue, 07 Apr 2026 02:39:14 GMT  
		Size: 2.5 MB (2527723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eab3abb1989fe117a2fc28fff1b6b63aa4f155728dc3e5befbd4961c062cd145`  
		Last Modified: Tue, 07 Apr 2026 02:39:14 GMT  
		Size: 11.2 KB (11215 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:10953608edb99a1ea8a73fd43a0cc2b7ebd3afdb4ce27dc1285b795f9b2f2eeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.0 MB (93022272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f76adfe783ee4f852503b0a63e4a32930fd28c623421fbfb8a01b1ea87ea351`
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
# Tue, 07 Apr 2026 09:04:35 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 09:04:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 07 Apr 2026 09:04:35 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2206a81f65df3147f8c62d4c01c47495515dae16f93ce6845cd7cdacdd206f1e`  
		Last Modified: Fri, 03 Apr 2026 15:56:51 GMT  
		Size: 34.3 MB (34313334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982a81f7bf5b29f9acb665db3784db3bbb0bee22151081054f4ff4c3cc572cf8`  
		Last Modified: Tue, 07 Apr 2026 09:05:00 GMT  
		Size: 58.7 MB (58708938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d024ab4a86e356e35066bb6eb407ead467fdcd450385f7913a219f0ea555a001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2537173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f9f9a9cb329338c26119acccdecab3c5f816ee2c856120b32fa79ed2408c1b`

```dockerfile
```

-	Layers:
	-	`sha256:e4af4b7dc54e9e02d63fc6fc3d97c9040f8e050fb010378b1faab7c6166c5f1a`  
		Last Modified: Tue, 07 Apr 2026 09:04:59 GMT  
		Size: 2.5 MB (2526060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dae06da17336d6eee944475e6942252777ff8fc26a2e416d3372fc45ac008848`  
		Last Modified: Tue, 07 Apr 2026 09:04:58 GMT  
		Size: 11.1 KB (11113 bytes)  
		MIME: application/vnd.in-toto+json
