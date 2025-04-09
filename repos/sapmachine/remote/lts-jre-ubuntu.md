## `sapmachine:lts-jre-ubuntu`

```console
$ docker pull sapmachine@sha256:76fc80865e60efd91e6f1993c51eb3c4966e1ce297777fac10c6625f634cd158
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:93fc18a368a3c13d0f412e24b64b5550521267768e68308ba5ad36531d4fe212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89830485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04eb92f64f0330f72a6ca327af2c56902bd3f301d7f50f2c15cac24cf5671c9e`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:13 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 13:39:13 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0c0572d73e601ad75a7c5249a4eadccb54f084d30ac61a141d2f5fd447724f`  
		Last Modified: Wed, 09 Apr 2025 01:20:53 GMT  
		Size: 60.1 MB (60112833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:af277f8c16a17237a881bdb3f899dca161af0d207f2cbcde978c9c7b7dc12904
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2398268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b89373579e5c7b54d91dd2fb1d9a63544c082a12b0e8ac8750768b16a7995a7`

```dockerfile
```

-	Layers:
	-	`sha256:e66161f093e6a129ac388914b03743db727b8f8129810fddd699b0c364d7565f`  
		Last Modified: Wed, 09 Apr 2025 01:20:52 GMT  
		Size: 2.4 MB (2387818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54a8c55d821dbf9948f4aa6a6cb91d27300fa4c20c35e192f9d361c50d96784f`  
		Last Modified: Wed, 09 Apr 2025 01:20:51 GMT  
		Size: 10.4 KB (10450 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:fc0ab7551ca5087fd9407d2d3f355471cf71d8e73fbc988f9a55cf7c7699c0e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88149556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3e25f6175496a9dd8a52661616e107a2ae2420da294ba56a4934494ad559e27`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:13 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 13:39:13 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bcc4db821ddf0a29be95297f1ddaee5fd66bfde88f148fceaf06ef691420a67`  
		Last Modified: Wed, 09 Apr 2025 09:30:47 GMT  
		Size: 59.3 MB (59302598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b019cac44429707fdaa9a4bd52e12caada8c47595028615c2e54a4af5a8c4ca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2398960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b46307f4763732f9ea4178befbe874b2906af6c970954a09949902b937c2b4c5`

```dockerfile
```

-	Layers:
	-	`sha256:088f610452a710d32e56c0ece47a1296225603ec2c602adf11fff0c74bf4a2a9`  
		Last Modified: Wed, 09 Apr 2025 09:30:45 GMT  
		Size: 2.4 MB (2388346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d56a3c39b1c8736132714318f342864ba7f6529689718d1e59c913c9ab07201`  
		Last Modified: Wed, 09 Apr 2025 09:30:45 GMT  
		Size: 10.6 KB (10614 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:eca0a809c5fd05d8e5bdc67d5386d78e4d3e386a779b83fdc34a56d990023921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.2 MB (96150360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83dd054d63ef0ae4ee57b2d398df5cbaf0aecc5eb4da869c92647a1f0fd36e9f`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:13 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 13:39:13 GMT
ADD file:d7a12d3d510b1bacf894dbb7d42f36de9391b0766c28643a60d20d3c37a12762 in / 
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7be894b3e11d60e6c310a10016f7c569f1a313b370ab3964114b1c135b1ce53c`  
		Last Modified: Tue, 08 Apr 2025 11:53:59 GMT  
		Size: 34.3 MB (34340867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92cc99fe8c0a6f7680363a4aecc595699f28b38f2c6970ec567c9a6538b4f2fe`  
		Last Modified: Wed, 09 Apr 2025 06:54:50 GMT  
		Size: 61.8 MB (61809493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c6a5694dcd2bad4f10b12bfac38d9b5d2ae6eb4315b70faf08570d9f54d5a0eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2402311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57cf0fb4e78dc2f7cee4fd27a065160625cdb05e094f5f3a90d827a2d28e225`

```dockerfile
```

-	Layers:
	-	`sha256:a4c030d02f8dcab4f50e45b10da9327c8dcfdc703a8bc7c28b616f9946f29697`  
		Last Modified: Wed, 09 Apr 2025 06:54:48 GMT  
		Size: 2.4 MB (2391787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7cb565ff2b1db10abdcf8077c6f7ffd43a4f2e71e84b771d57681fb82c2d1e5`  
		Last Modified: Wed, 09 Apr 2025 06:54:48 GMT  
		Size: 10.5 KB (10524 bytes)  
		MIME: application/vnd.in-toto+json
