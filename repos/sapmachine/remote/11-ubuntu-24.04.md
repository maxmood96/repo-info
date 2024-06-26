## `sapmachine:11-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:9ad5741f7a6cbff883a9cc2136231777239ca1de58a922ff3544fb288cc85584
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:900860d4893712a15a0427eb74745a828f1c5d30c991e9300a0139deb1190870
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.8 MB (230774985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be5bf7fbd0c02a340f7a024227a5b74f348ff4a17580fb977e81003dd302cd01`
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
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
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
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0380c9e1dbe05c6be600d492433ced034dbbbf587f5c0ea7926ac084f8828f7c`  
		Last Modified: Tue, 25 Jun 2024 22:59:14 GMT  
		Size: 201.1 MB (201069832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:93ca93543bed2e3bda60f7bca6601324d3ad9c10bc93cb0473c2d66e020ce5a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2448077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07af2e5d7cbc47103f651837170341425c042c6260042a51c7046979bfa79b83`

```dockerfile
```

-	Layers:
	-	`sha256:af9f15a2388b9722f5182edf43910f5c14f65d0589699ba2631c448468776c6d`  
		Last Modified: Tue, 25 Jun 2024 22:59:10 GMT  
		Size: 2.4 MB (2436919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:756305b2d80b91769e5ff430807e73109e77854b39b6b0d858a710c0eb3a9e80`  
		Last Modified: Tue, 25 Jun 2024 22:59:09 GMT  
		Size: 11.2 KB (11158 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-ubuntu-24.04` - linux; arm64 variant v8

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

### `sapmachine:11-ubuntu-24.04` - unknown; unknown

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

### `sapmachine:11-ubuntu-24.04` - linux; ppc64le

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

### `sapmachine:11-ubuntu-24.04` - unknown; unknown

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
