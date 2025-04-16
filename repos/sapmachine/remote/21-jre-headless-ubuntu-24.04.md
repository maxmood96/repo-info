## `sapmachine:21-jre-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:fc87fbdcddcee0189f8a457099f3211541bd108a2216d205a493f0fdc9fd92c9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:8f825382b7609ab9c39c1de6a14917fba26525c73e4ae82684c993fbda184516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88650355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e25f3cd55c3012ba4cf4e7d40d2568367a59cd53f2df214bc002eaf452ba63f`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 08 Apr 2025 10:43:12 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:43:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:43:14 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Tue, 08 Apr 2025 10:43:15 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2a1be5d2b5698924b2ce95f52eb155d8c2e238e26b5ad8f7e0aeedbae1b5e0`  
		Last Modified: Wed, 16 Apr 2025 16:13:52 GMT  
		Size: 58.9 MB (58932703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0600e79061364d466e9be6f380066cb78b432c7de2ca2c471d752df314b1b1a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2161635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4d41eeb6423703088659ba65d2184a62b20835c80230efec7d2449eabe5b787`

```dockerfile
```

-	Layers:
	-	`sha256:5d00c4fee93ab1925154654c4d7ef235cab180a87dc2720799cddeeb6e5fbd48`  
		Last Modified: Wed, 16 Apr 2025 16:13:51 GMT  
		Size: 2.2 MB (2150984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:442bd56e2051aaeee81f338a3bc923791cf342392f7aa3b54337b8340c1f4afa`  
		Last Modified: Wed, 16 Apr 2025 16:13:51 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:23c269989796a1034aad87f3535fad4c43de25b976ff0ff7edd7f11a8a1ee9b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (86962654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:435bda74582d1ff05e5503685fd2e9879e740c4b9de1f702f9e672547aa1caac`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:09 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:46:12 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Tue, 08 Apr 2025 10:46:13 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9c45ec5239e5fbce4838f69ba317a71017e87a61bfc95a4356566439f2e1992`  
		Last Modified: Wed, 16 Apr 2025 16:28:26 GMT  
		Size: 58.1 MB (58115696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b7550a4238a753dd33ecf867c7ee9f0e855d8a6b17a414ed2ae42f227c57521a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2162318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a53f318f0709b891bc63fab6363cca4be0dde895d83d1aac84ef7dd5a39efd37`

```dockerfile
```

-	Layers:
	-	`sha256:5d62971ffb2f9f582d6e98849c676025f14957491e25e474db59afdd527cfffd`  
		Last Modified: Wed, 16 Apr 2025 16:28:24 GMT  
		Size: 2.2 MB (2151503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66d91c38d0e631ce53b1e19a04e9c1e7510eb936888cfe3c233ba4d04705761a`  
		Last Modified: Wed, 16 Apr 2025 16:28:29 GMT  
		Size: 10.8 KB (10815 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:13315ba16ca5001f35be2f0192c974d30e902dd98d8804a129e9fd45edea511a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94762474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bc87b03cd59cf9512224e915a33cdf7f74d1497ae344cae83192f53333dac40`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:11 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:46:14 GMT
ADD file:d7a12d3d510b1bacf894dbb7d42f36de9391b0766c28643a60d20d3c37a12762 in / 
# Tue, 08 Apr 2025 10:46:15 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7be894b3e11d60e6c310a10016f7c569f1a313b370ab3964114b1c135b1ce53c`  
		Last Modified: Tue, 08 Apr 2025 11:53:59 GMT  
		Size: 34.3 MB (34340867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46911646b309ef8def045c5b1f6093318cf55a109b49c57b8fb7812742eed23f`  
		Last Modified: Wed, 16 Apr 2025 16:45:33 GMT  
		Size: 60.4 MB (60421607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0a8012415f4951559f4be2b1921e45782b4f85433057dd13843357f172e3f37f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2165614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8de0bec2cb2067583b35324e57f3dd4b833275dee34b4938f3631004076648b`

```dockerfile
```

-	Layers:
	-	`sha256:b622e9266f4847410394637ba7dfe1bcb8641fc33f5038d24414d364812db8d2`  
		Last Modified: Wed, 16 Apr 2025 16:45:31 GMT  
		Size: 2.2 MB (2154890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80f16e563d754eab1e180155b1ad27bb8746a91ed74fb597087fec2b27655ea9`  
		Last Modified: Wed, 16 Apr 2025 16:45:30 GMT  
		Size: 10.7 KB (10724 bytes)  
		MIME: application/vnd.in-toto+json
