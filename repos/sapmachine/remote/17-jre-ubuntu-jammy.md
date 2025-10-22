## `sapmachine:17-jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:363d03c61b0bafeda657dbbf0141c8ac89a0c681c603fedcadec3786c1ec9053
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:7bae74043b5b8d70ebae8239d68c846c2dfb3f5832bc3584355f6381953c478a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.4 MB (83409267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b27753f0d0b8bf83233aab564a309210002f33d18db50b50e9c575791bac0aac`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 06:09:35 GMT
ARG RELEASE
# Mon, 11 Aug 2025 06:09:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 11 Aug 2025 06:09:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 11 Aug 2025 06:09:35 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 11 Aug 2025 06:09:35 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Mon, 11 Aug 2025 06:09:35 GMT
CMD ["/bin/bash"]
# Mon, 11 Aug 2025 06:09:35 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 06:09:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 11 Aug 2025 06:09:35 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1ec8d06ee827d9e2c3af0b8795885bb8c583e2081bd19d8774496aa954e3ed`  
		Last Modified: Thu, 02 Oct 2025 05:20:20 GMT  
		Size: 53.9 MB (53872449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:44ba98773b08a135f535045c24f959bab1da31355d49875d9903358d976f11e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2552456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6147b207581002cd49fe3534de4b2524af4b8c6d5b278edf17769864b3a3429f`

```dockerfile
```

-	Layers:
	-	`sha256:2edfda27aad12858b1eb68d6c349401b7f2a720eeb5c22e66072daf9425087e1`  
		Last Modified: Thu, 02 Oct 2025 09:07:29 GMT  
		Size: 2.5 MB (2543639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47aaf9a9dc4826680f16009700ff45820b5b2f454a8b7c521a4153de86c6edbf`  
		Last Modified: Thu, 02 Oct 2025 09:07:31 GMT  
		Size: 8.8 KB (8817 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:920631d68d686013b8345b63cb6b250f015fdeca974a76b91f60571d40aced2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80694522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45baa19343a8e94b95bb1c1180f3bc4938e41a7bc6e73d1dd9019b265c16e244`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 21 Oct 2025 21:30:22 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0447056a045cf6361c02fc376dff61f7a9083661744c829f60d7c9f487b6e2`  
		Last Modified: Wed, 22 Oct 2025 00:06:50 GMT  
		Size: 53.3 MB (53311415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b56e9159f33b1504a632902f9544f5522c848a391fed832b07dcc08c3effe469
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2552242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e3c9a78346abeb2286db72f0cc53ebd0468a108e884589ed233e01c8ec863cb`

```dockerfile
```

-	Layers:
	-	`sha256:9d478b9f6eec94862bd5e3e7617d0557f12c039a5e7d9dd4989d59cb0d47fcd7`  
		Last Modified: Wed, 22 Oct 2025 03:05:41 GMT  
		Size: 2.5 MB (2543321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d32f5b5e44e97a34b5ebc3a850e965f409fdcf1018e5df92ce159d2a883e2c70`  
		Last Modified: Wed, 22 Oct 2025 03:05:42 GMT  
		Size: 8.9 KB (8921 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:6700ebc45a9cff80b4a4df6af7ac9f8a064d4d9b7ab0ccd606e47184c65ac2d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.4 MB (89391562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:618a6a65aaf629d339e546fc309140b6f551d1d6bf3764a908a414c91db98f97`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 06:09:35 GMT
ARG RELEASE
# Mon, 11 Aug 2025 06:09:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 11 Aug 2025 06:09:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 11 Aug 2025 06:09:35 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 11 Aug 2025 06:09:35 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Mon, 11 Aug 2025 06:09:35 GMT
CMD ["/bin/bash"]
# Mon, 11 Aug 2025 06:09:35 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 06:09:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 11 Aug 2025 06:09:35 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4259d8033f30bc4b649845e2525112964031b105224cc1ebab96c79633621343`  
		Last Modified: Thu, 02 Oct 2025 04:53:16 GMT  
		Size: 54.9 MB (54944773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4d298b32060629a4b9c4656a063f2ca15e3e2388ea5349296293ac7517f8cda4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2550615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4498495c8cc5767502832b98078aac26a227cc0ccd36f54ea8073845a4199b7`

```dockerfile
```

-	Layers:
	-	`sha256:f9c06c66cafa218abc6c78d9b02d6679ad5d760df2e1c00b07eb318e7fdf629c`  
		Last Modified: Thu, 02 Oct 2025 06:05:51 GMT  
		Size: 2.5 MB (2541754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c54b8e66ee3db410b9cdc9e5fb787344d35f879440410fdddcc2b072055c8b1`  
		Last Modified: Thu, 02 Oct 2025 06:05:51 GMT  
		Size: 8.9 KB (8861 bytes)  
		MIME: application/vnd.in-toto+json
