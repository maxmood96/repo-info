## `sapmachine:23-jre-headless-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:c009fc61487617815435ffb997bdb89cc69d41311e96af158ef1cd9d364c7f97
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:23-jre-headless-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:49104d62c7b4cfab85fabfb94a787dbc54de85810a51e3bbecca9baa238059b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.2 MB (85228181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e182436104f7c37ba6cf58a65eec00b407259a7d292c6868d103108e4ebfe1c`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:32 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:34 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Wed, 18 Sep 2024 04:18:34 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre-headless=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3823320faa42774534fd7eee0bd245af8cec6a720ad722144d40efa229291d8f`  
		Last Modified: Wed, 18 Sep 2024 05:32:37 GMT  
		Size: 27.5 MB (27511052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de67f5b0c3389b7c868171d7b3cb2889c6fdc96fea79d8ef286de3b34740eda4`  
		Last Modified: Wed, 02 Oct 2024 02:00:00 GMT  
		Size: 57.7 MB (57717129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jre-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:fd245f2f2b25098152397e2c93319bae0175b5a717fa5355ef08edbe5f5e7a63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2054136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9e8d8767ded616556f8085f943e996d0466e053209e7bf8b6adc68682129d47`

```dockerfile
```

-	Layers:
	-	`sha256:30c7e8ee9cda76f0af79bea663e21e18cdef2a4c8a4547b88d1d0b1eb097fdfc`  
		Last Modified: Wed, 02 Oct 2024 01:59:59 GMT  
		Size: 2.0 MB (2045498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9a05ea157f9112cf8b3035c227190347ff61afe181640b28f5eabf74d94231f`  
		Last Modified: Wed, 02 Oct 2024 01:59:58 GMT  
		Size: 8.6 KB (8638 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-jre-headless-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:4e3b26d1309b5045f21c8ef39a26b66c9b8dcaa28045d278a296a7b536f0f0b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82730701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3281f9ef7cd0e10fa99c412ccc32a5566263ab744a444055163e58f390f8bca`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:13 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:15 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Wed, 18 Sep 2024 04:18:15 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre-headless=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f7087ec3f63a82386ce40d74d075d761ece5bfaefdc30b9ef62f73ecfb2e41fe`  
		Last Modified: Wed, 18 Sep 2024 05:32:46 GMT  
		Size: 26.0 MB (25973592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d953ab450791207b3c4a772c7deed3bf77a115bc0bce70c8fa3b9edca61e43`  
		Last Modified: Wed, 02 Oct 2024 03:48:35 GMT  
		Size: 56.8 MB (56757109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jre-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9ca4361ec2ab1ff45f58ffaf7216fb1aa4653bb78643e20ede217028fc2531c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2053230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:263eaf34e242736228a6814334dff64fa59ebddd1c68d891556c96dbbe88b180`

```dockerfile
```

-	Layers:
	-	`sha256:b973fa8dd4fb12a8af8457cab1eaf1959d7daf1a8c334ba5cddeadad56049406`  
		Last Modified: Wed, 02 Oct 2024 03:48:33 GMT  
		Size: 2.0 MB (2044494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab54f9a2d423f9d45f2cbaa3e0a9b45216b943a67334b009a9f3b527843150b7`  
		Last Modified: Wed, 02 Oct 2024 03:48:33 GMT  
		Size: 8.7 KB (8736 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-jre-headless-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:a49050c9a7301b6360029645fe604df956b9b538029b34ba01864115c9eaad4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.6 MB (90635624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cedde9699c125f7f38d6cd1e584d44a3d5f1646e8e609620a31792f0fc327e04`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 18 Sep 2024 04:19:24 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:19:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:19:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:19:24 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:19:28 GMT
ADD file:c6515e5ea6494efa348e1177d50c0c28bb8236a5d2b518388f13b7d5a528d4fd in / 
# Wed, 18 Sep 2024 04:19:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre-headless=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cafd57629abc05d597016161b87b83b544a17d39d1016cfb289a60295fc7d492`  
		Last Modified: Wed, 18 Sep 2024 05:32:58 GMT  
		Size: 32.1 MB (32076334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ce6505a14e36b0b4136b7c6474d12ef0884bc2ba671c6360b8e57c63629420`  
		Last Modified: Wed, 02 Oct 2024 02:55:59 GMT  
		Size: 58.6 MB (58559290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jre-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:79f6b5c56894ba3d08720bd1038be496eb3aed15e72026488388ee4211cb544b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2057245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81e0c90cef4fc16ba35befc8b726f5e70effb549351e144c2b099e4a555fa825`

```dockerfile
```

-	Layers:
	-	`sha256:c991b8e76e5b3b81f220b934b5ac22e8e519111a003dda1011addddff7893974`  
		Last Modified: Wed, 02 Oct 2024 02:55:58 GMT  
		Size: 2.0 MB (2048569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c91a480ef8a4e785fd1ab1c184894c23a7300d6eb7dba754c0c6dc017965c630`  
		Last Modified: Wed, 02 Oct 2024 02:55:57 GMT  
		Size: 8.7 KB (8676 bytes)  
		MIME: application/vnd.in-toto+json
