## `sapmachine:24-jdk-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:99c6204eaddde53b2dbf44b1a24ccbe99a8c3ecca7c2b0cd0afb1a8b19bf0010
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:24-jdk-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:2d5d9d5d4d090a3272eff817f16f25c338d7eccc0a4d498007524d7e5ba7ce8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.9 MB (260939202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc18c5582f3a29549e219aa407af524738bb67faab5a421aa7b42670987e0693`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 19 Mar 2025 14:31:37 GMT
ARG RELEASE
# Wed, 19 Mar 2025 14:31:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 19 Mar 2025 14:31:37 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ce9abe8382509dfe8f9aa874c29f43898e3a097c02e6815bac402844f2a58f`  
		Last Modified: Wed, 09 Apr 2025 01:20:45 GMT  
		Size: 231.2 MB (231221550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b407b66920374d1dc6e2b56a2f4930bcd2502fea88e57aa8892f83cec1b0b19b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2233687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b9511db534dcf19013c53826ea703a1c36b6a78e499df23501dff969181cd79`

```dockerfile
```

-	Layers:
	-	`sha256:a624d3366c1aa334ab7215e0aa77b3513585512f3e7d8700d6b92ce57fc2e868`  
		Last Modified: Wed, 09 Apr 2025 01:20:41 GMT  
		Size: 2.2 MB (2224129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec3ecff2c3b4dd86076b75dd0d8d33074c597f6d4fab8ce77e4aa840f0bc5589`  
		Last Modified: Wed, 09 Apr 2025 01:20:41 GMT  
		Size: 9.6 KB (9558 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jdk-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:2c2a51f4a0c81fca3dcaa8cd8fcc724f937a2192eee3aea586e8c182591fb981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.0 MB (257991953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0642ab5844dad0d33edf228338b6ba0da26851a144c5c3574ced64d7ca33434`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 19 Mar 2025 14:31:37 GMT
ARG RELEASE
# Wed, 19 Mar 2025 14:31:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 19 Mar 2025 14:31:37 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f78d6db90a5240a34d653a60266f9ae87f67b07fe35946bb9dbc6dacf8540c9`  
		Last Modified: Wed, 09 Apr 2025 09:18:46 GMT  
		Size: 229.1 MB (229144995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:78409770d77c8a16dcb9ff5915a55c44d70d72a9a4feb10f156c3b22aaaaa026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2234295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7057c415929866767b1e36ff96d9501ddcbd2b970c30988004ad8d716d15c9a`

```dockerfile
```

-	Layers:
	-	`sha256:dcdbf21084fc0125aec6e6d59ba6b339691072c7887a3291974878fc59312ede`  
		Last Modified: Wed, 09 Apr 2025 09:18:41 GMT  
		Size: 2.2 MB (2224609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcafc277dc759c7baf7e1506808a432c5e86b1e9cb8c7c605060db216e60a248`  
		Last Modified: Wed, 09 Apr 2025 09:18:41 GMT  
		Size: 9.7 KB (9686 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jdk-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:df6565db4f03724d8e3c6160f0635014c880c1bc43f3a8d802e6698eccd0a7bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.7 MB (266702269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b06298983a52f4b730d61f5050db059ca2c36499e5f39c2506c0af05cbdb9bc`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 19 Mar 2025 14:31:37 GMT
ARG RELEASE
# Wed, 19 Mar 2025 14:31:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 19 Mar 2025 14:31:37 GMT
ADD file:d7a12d3d510b1bacf894dbb7d42f36de9391b0766c28643a60d20d3c37a12762 in / 
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7be894b3e11d60e6c310a10016f7c569f1a313b370ab3964114b1c135b1ce53c`  
		Last Modified: Tue, 08 Apr 2025 11:53:59 GMT  
		Size: 34.3 MB (34340867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08dbd775d352df345f3ca29aa7e24e6a5ce65ba049960034829c32de5bbd698e`  
		Last Modified: Wed, 09 Apr 2025 06:34:33 GMT  
		Size: 232.4 MB (232361402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3e62f2e0a1e246fbb538c4abbc75ef4288035628e7509b11158d8de64f3b339d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2235067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a3668958c52c212acca9e0885ec059181bbd35d38020013ba13bbab8f1fefb2`

```dockerfile
```

-	Layers:
	-	`sha256:92682ca863b3d475ea4ab411876814d344177d95da1594a00692ba4ea094c987`  
		Last Modified: Wed, 09 Apr 2025 06:34:27 GMT  
		Size: 2.2 MB (2225453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24653b44dd8df1e6a87c021712dcc0578f37ff801698ab26308c23cab5fd553b`  
		Last Modified: Wed, 09 Apr 2025 06:34:27 GMT  
		Size: 9.6 KB (9614 bytes)  
		MIME: application/vnd.in-toto+json
