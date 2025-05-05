## `sapmachine:lts-jre-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:faa52900f5033dbd5e909be478d377d6c5c8297c70345c19fe4a8e3e30cb0f4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:2d4df64c5174ed106296efa676258a00eb3b7d89a76ed692e3a1e353005237db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88650155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2bca034c9ddbb60d3bebb66c19ec5ce45d7df9211c2eb9f6fcdec43085e1b18`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5436a964c367eaf43220504a32b874f8b1ec398b4e8770093e93101ac83c63`  
		Last Modified: Mon, 05 May 2025 16:36:46 GMT  
		Size: 58.9 MB (58932626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:424854fca299fccf645111603fb29318978cca42420604c3e4cd7aa85237af2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2161639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2f603ba9558476c522c021ebe51503b3aab0d2f9f2f01ba3c7a208a1b2a9976`

```dockerfile
```

-	Layers:
	-	`sha256:af630b88da8898d05fe8c26a3a328b4371b2457882bc1efb1abaf5ef7ad7bed1`  
		Last Modified: Mon, 05 May 2025 16:36:44 GMT  
		Size: 2.2 MB (2150988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4f1c1d7c7873050f4ed5dfdd62fbc99f577e0556c5ac59541dea281ba477a31`  
		Last Modified: Mon, 05 May 2025 16:36:44 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu` - linux; arm64 variant v8

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

### `sapmachine:lts-jre-headless-ubuntu` - unknown; unknown

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

### `sapmachine:lts-jre-headless-ubuntu` - linux; ppc64le

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

### `sapmachine:lts-jre-headless-ubuntu` - unknown; unknown

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
