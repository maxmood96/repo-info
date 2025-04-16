## `sapmachine:24-jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:7f472b16a63ef68194aae03ff06ac6700349dda411459b7ed348b179311e2e64
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:24-jre-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:d48caec8d1afe67f742b7946e2ede9faf5a59097fd0becad2f9c9671ef1043df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97212473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecf44d9db011315d60dffd231966c5df2cbc69352b2623d064634b6b9644865e`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 07 Apr 2025 07:24:14 GMT
ARG RELEASE
# Mon, 07 Apr 2025 07:24:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Apr 2025 07:24:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Apr 2025 07:24:14 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 07 Apr 2025 07:24:17 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Mon, 07 Apr 2025 07:24:18 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ef552ec62802b43506bfbe05ea1ebc7bca389f89b5e993e4dd0b22f22a2262`  
		Last Modified: Wed, 16 Apr 2025 16:14:04 GMT  
		Size: 67.7 MB (67680108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:afa9bfbc918464e577f9c5e3d3f49164c3c9e34c3902949103a210e11cf53a48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2425872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ff11f2fd1d913498bcbe82b0d49fa86d3b154d89002fed7078b7598002050a5`

```dockerfile
```

-	Layers:
	-	`sha256:d7a6803bdd3886ebeeada006b8426ba3699a5f650d052dba130c92f6c4b5482f`  
		Last Modified: Wed, 16 Apr 2025 16:14:03 GMT  
		Size: 2.4 MB (2416408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e644d2f230795143af669e245d8f8609f8fd08c1255c50f0ef193e907aad8177`  
		Last Modified: Wed, 16 Apr 2025 16:14:03 GMT  
		Size: 9.5 KB (9464 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jre-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:fe772b44055c7a4c2dedfa0cb9cc0e079841eebec34039ff3ca8523f111373df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (94029205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17288238889c88a2fa7ba7fe013158e725506efb973692833b5dfabe0769c298`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 07 Apr 2025 07:27:02 GMT
ARG RELEASE
# Mon, 07 Apr 2025 07:27:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Apr 2025 07:27:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Apr 2025 07:27:02 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 07 Apr 2025 07:27:04 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Mon, 07 Apr 2025 07:27:05 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e0283fe47f684cc546f37a7d19bbad7116fd4fab99aef403fcceaa99159c4c`  
		Last Modified: Wed, 16 Apr 2025 16:19:54 GMT  
		Size: 66.7 MB (66674974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5279cbbf15adefd8fb0aa6029be66f80e9c58f872fb249c9453a7f937f7f2465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2425703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84bfbfae7bfa14356e1cc42106b7d9a4c140ec3b1f7bc91f9d19890936568460`

```dockerfile
```

-	Layers:
	-	`sha256:af2cd0d32c05f610e335a9603ce87d89c112bf441944f6de716ac1365ae841ab`  
		Last Modified: Wed, 16 Apr 2025 16:19:51 GMT  
		Size: 2.4 MB (2416111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44962aa0eb9e78364b3b1e79b2254ff1df375d6a5456f0ccafd4e1c5ca372bd2`  
		Last Modified: Wed, 16 Apr 2025 16:19:51 GMT  
		Size: 9.6 KB (9592 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jre-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:384bba76e2b10460e977bf2583411caaa4ff29c18132be0dda97f09fb35b079b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.4 MB (103392885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c04581f16d3c1e587f91c9abfc0500cc7d405f14dedfcd40166320c2c5bdf346`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 07 Apr 2025 07:25:40 GMT
ARG RELEASE
# Mon, 07 Apr 2025 07:25:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Apr 2025 07:25:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Apr 2025 07:25:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 07 Apr 2025 07:25:44 GMT
ADD file:b1634c9c9ee669b835ef39787fc71f78267fab0678a8e8c5547ba2339762e075 in / 
# Mon, 07 Apr 2025 07:25:45 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:220e8fedb927c1ecfafdf1e8cd0a85977de62e4afd95df2c5a27a70d3bdf34b0`  
		Last Modified: Mon, 07 Apr 2025 08:26:45 GMT  
		Size: 34.4 MB (34442696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:804bedd952b039f64d585f60f4e01874ac72443829da0e7a7ba117940a9dc1e3`  
		Last Modified: Wed, 16 Apr 2025 16:27:47 GMT  
		Size: 69.0 MB (68950189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d2db5122b63cee5a7e7ab89629c8138efb5d61c3d785e105202266bb586520cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2429290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a83ce63bb2f88909f04112383e16b9a072995d7ac858aa3663bd266a1ebe1c3a`

```dockerfile
```

-	Layers:
	-	`sha256:346846d3feb90e844b2161e8af45dd6da47413794010eef1c71b8e63e5d0306d`  
		Last Modified: Wed, 16 Apr 2025 16:27:44 GMT  
		Size: 2.4 MB (2419771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ceee9e3458bedf133aad0f51a2acfea93bb4c5d7b91344f1b5812f59b82021f`  
		Last Modified: Wed, 16 Apr 2025 16:27:44 GMT  
		Size: 9.5 KB (9519 bytes)  
		MIME: application/vnd.in-toto+json
