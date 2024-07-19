## `sapmachine:11-jdk-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:5c28611909e3e47239c2c188a5664a6bcf8a897fef036511f0a41bb29bed3d52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jdk-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:bd4360227c0ae82675cd886c2142fb33741769b93fef72db731e202c0ee5d017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.8 MB (230823676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dad36a13705f2653e4cdc2679d85c4faeee5aadc0642283293062362e7b9a2b`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15394dc155969a70dad5e8d723729787d6852b2618ff7fb938880de7f91f7a48`  
		Last Modified: Fri, 19 Jul 2024 18:00:23 GMT  
		Size: 201.1 MB (201118523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5af64ddb8d120bea04a601c5d94f731429ffc79f270cfe8ba733857a5b062722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2474236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94f762608afea6f4e07b56d5634c7b1f7c4b9d76d51cc1d9d3365337b1fd56e9`

```dockerfile
```

-	Layers:
	-	`sha256:13c6720c555c00bdde2a2f64178e18b5de021b81b19cd5909dc302a9f45dd0fb`  
		Last Modified: Fri, 19 Jul 2024 18:00:21 GMT  
		Size: 2.5 MB (2463097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:648ee194b973c91e403d75e3028a1ffbd1cae6bb00330583653263f61cee086e`  
		Last Modified: Fri, 19 Jul 2024 18:00:21 GMT  
		Size: 11.1 KB (11139 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:bf7aa3cdb97205cd5c3d7f5f0dac0acc28c8b4ee6042f43bab629eff7f19a159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228443585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3f52bc9002becef66d376c66b285d0f41191069758b971c4b0ebf7980ed3b0e`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:56 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 13 May 2024 10:06:56 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Mon, 13 May 2024 10:06:56 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:56 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 13 May 2024 10:06:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af178449a3d82005e4e48274e80ac75903c7d77ba094ecad224cc32372a13c78`  
		Last Modified: Wed, 26 Jun 2024 00:27:41 GMT  
		Size: 199.6 MB (199600542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:933b2caccc8209249f8380a138cb09ae5735051ac0e30e16d06be2213ed421e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2449665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28973c2e95805c1c1e4ae765d50bf5678d7bab1899585fb678be3630b173d00c`

```dockerfile
```

-	Layers:
	-	`sha256:4c814701660440897e314386cca0b20d2fad702d1c84d9b92c109f117edcc112`  
		Last Modified: Wed, 26 Jun 2024 00:27:37 GMT  
		Size: 2.4 MB (2438110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3b687d76ed2ec93c29b0b763f584d0ea573131c63c1e3ede7936cbc2e939a91`  
		Last Modified: Wed, 26 Jun 2024 00:27:37 GMT  
		Size: 11.6 KB (11555 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:b51dbd9f112f8e9a84a9bd4ab659930568761103d7aae5c3d23a4b18be9edf2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.4 MB (222374972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c9fb263810ca4db3778a4e6593b1335cd3d256e72a55cbfc2f08072a015c0b`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:56 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 13 May 2024 10:06:56 GMT
ADD file:e767a66d1508f3628411abaff75d39ed1d6261596c668fa88252ed9a584e7fa4 in / 
# Mon, 13 May 2024 10:06:56 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:56 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 13 May 2024 10:06:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:875c01bc1b3e6b966440b42d40365968bfdd742c762026b5739c5d1f493510d7`  
		Last Modified: Fri, 07 Jun 2024 12:11:45 GMT  
		Size: 34.5 MB (34506029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c261f20e9a3447e9908f9559659ef384c65fd4c23b252312dcbee3d703b2e240`  
		Last Modified: Wed, 26 Jun 2024 01:08:08 GMT  
		Size: 187.9 MB (187868943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3d0e0f752274bd312314079554f0666efff187bc71a55d9643ec71d29995c1f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2449574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de5c08519e8a120b795652bfc6a8d8e16003cb8ba492367a0a5a0d119113f14`

```dockerfile
```

-	Layers:
	-	`sha256:25d594843bf310b90900b7fbb2f213b988784abfef67c571e57a510e1e056a01`  
		Last Modified: Wed, 26 Jun 2024 01:08:04 GMT  
		Size: 2.4 MB (2438330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73991dd29b3f201635dbe9f299744e3a1b30f8e04835b342eea987d41f477f1f`  
		Last Modified: Wed, 26 Jun 2024 01:08:04 GMT  
		Size: 11.2 KB (11244 bytes)  
		MIME: application/vnd.in-toto+json
