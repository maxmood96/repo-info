## `sapmachine:11-jre-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:be2ee43fb32d2138edf0d599fc77ddefd6c109f1a19b0f4398470ada23475073
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jre-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:2b62ad2ae998db6fe5a833673d16974c28027646d2802f7bc65edf5f5004d26a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79492603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:781a6f70beac34662c0e1826367c1411843f6e6448f98870dcd6a660dc3eacb3`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99014950e9e112700b6519cac77e8e06c643df25677f347695025700c2e1373`  
		Last Modified: Tue, 17 Sep 2024 01:00:50 GMT  
		Size: 50.0 MB (49956915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:67801027e6a9f915f22af1590cb5560ec83ade1c6ccb0f3eaeb305510700c1fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2407495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8291390bc338e63fd3cfea1d74dc476ba1f94186b299c61d7eb3fd1f6cd7430a`

```dockerfile
```

-	Layers:
	-	`sha256:88bf778b7d89b59273a64c965dffea7e092cc419332112748dc07e9770ad7f5c`  
		Last Modified: Tue, 17 Sep 2024 01:00:48 GMT  
		Size: 2.4 MB (2398928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d24c640a37b5f88529dd5994d5de87464739584590e24e0b673f2fa9cc8b448f`  
		Last Modified: Tue, 17 Sep 2024 01:00:48 GMT  
		Size: 8.6 KB (8567 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:5733ed68e150c2b60253a9a92bd3c207e9da601fc084cd9c34ce911a3f790c93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76598271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60dcbb05f49e7f60d11430e967cd0e5c4240fb58b7a28b03c1f4b49f4752a4c3`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87767a1125db418f3ebb66000e709da135a9650d3906a5d119ed8ca26787694e`  
		Last Modified: Sat, 17 Aug 2024 04:47:32 GMT  
		Size: 49.2 MB (49239588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:16f23125b643e32cbe1429cb13fd41b78c78a6575f0984cfc19cb32ba9709884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2408104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f42a80752ce653288e17309ff7e293e4703a6f7f2e4ea6b4fbb61c2b343eb85`

```dockerfile
```

-	Layers:
	-	`sha256:13694aa1c7b846db8b6f5340b4bc63e03f9cac8b7a4a1b2b380ecfd9db95b39d`  
		Last Modified: Sat, 17 Aug 2024 04:47:31 GMT  
		Size: 2.4 MB (2399236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c171ba625c745411eaf683b39668059b6268168847878b2257d852e780ffff73`  
		Last Modified: Sat, 17 Aug 2024 04:47:30 GMT  
		Size: 8.9 KB (8868 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:ef16c6f3ed4c3464f36cbb1ad5ccff2ee59e2e8fd0d61a73fb6f29e2a26699ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.0 MB (83049312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37da4aebc03e6993ea9066758f37ae7cbf52473f683d5b621bab130907be9e8d`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:593b8356181268f4632d882f9f41d8b565910ac10009886043617c157fbfcae6`  
		Last Modified: Tue, 13 Aug 2024 10:45:08 GMT  
		Size: 34.5 MB (34464178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d37ab312c6df0070d9f96dafaa61751621f8432ce742c6599b0c139a02237eb0`  
		Last Modified: Sat, 17 Aug 2024 03:36:59 GMT  
		Size: 48.6 MB (48585134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:53224c5d48a77eacbe60734336d85cc6d8d708c8c7e934b560af963e17da4f39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2411518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42c9e84697f5c6b0948953b66a5596c7d7c119f4bb56948b283bb9cfecf0df92`

```dockerfile
```

-	Layers:
	-	`sha256:fad80b64fafb5f0ec506b5ef818f50dedc75a72b908ad3870f8ce59feb7ac257`  
		Last Modified: Sat, 17 Aug 2024 03:36:57 GMT  
		Size: 2.4 MB (2402913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b3288f8f16fcad845f24d45870f53273fca6d1439cdb2fbf0baf0d5b2fd9ec2`  
		Last Modified: Sat, 17 Aug 2024 03:36:57 GMT  
		Size: 8.6 KB (8605 bytes)  
		MIME: application/vnd.in-toto+json
