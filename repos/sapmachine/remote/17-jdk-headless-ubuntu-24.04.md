## `sapmachine:17-jdk-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:2c7728e5e15fbd0528485d6d2914ca62c7f538e7f120c226ec0d96361b1936dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:b58005e19a212fcad81e3fc35c91af24eef4aa2e432f9e1a76427dd4a58fceea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (229020129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c8667fe6dbbb3179670e54326c51fe2507dc00117de742e31dd2620f3f7304f`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:11 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:11 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04eb0acc4aab247e64ab07d6abd14a90394716485edc6984a01bfa99ac50ea5d`  
		Last Modified: Wed, 13 Aug 2025 00:37:12 GMT  
		Size: 199.3 MB (199296914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3b1807139a3fc961d9da0c57e43b2606842c026eea7078900a7e9983931995ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2364745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b172d108f4198fc647ab16d750336af3156d074b65318487f00a393537dc278e`

```dockerfile
```

-	Layers:
	-	`sha256:8a5479656aa31eed71c2f305049cb8f067a8bebdafcc41bded183fb582f3193d`  
		Last Modified: Tue, 12 Aug 2025 21:05:32 GMT  
		Size: 2.4 MB (2354468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40e5ca4a8198fdc803df6ee27709c533de11bc5b839aa229f8daef4ba992ee26`  
		Last Modified: Tue, 12 Aug 2025 21:05:33 GMT  
		Size: 10.3 KB (10277 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:cf75ca828f21f8c7ae6557c05469a0e5ec7a7ce07ebdcf5ffc44509d8e2500f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.9 MB (226871504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c321329b1a7278ed4f9ffca050bd05a47a1e03048c0b7329f9a001dc0d68a577`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:11 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:11 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e1094488cc054905670381d1ac74a51c9f36d644a02a4f7115980ddefcea47`  
		Last Modified: Wed, 13 Aug 2025 16:47:38 GMT  
		Size: 198.0 MB (198011127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d4068adecfaf24d0baa0d8fa3e11281e07038ea320fe0da8c7be6f2c190ce005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2365404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2779a09a7572afd4c90c97ff16553b197ca42e9a3aed9599d7f5d1015417b349`

```dockerfile
```

-	Layers:
	-	`sha256:47c397966c712f41ac6d99c4872b60e0196e679b4bb3a797bd102a085a94b640`  
		Last Modified: Wed, 13 Aug 2025 00:04:51 GMT  
		Size: 2.4 MB (2354975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:035ca21667bf3b80f2de5e83550d770d55cc4db2cdadfaac0b3041501fbc4e9e`  
		Last Modified: Wed, 13 Aug 2025 00:04:52 GMT  
		Size: 10.4 KB (10429 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:650130d56d2d129682869b001f6226ff5ec366bf123b422a924a5deeb6143630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234204187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4179b96d3b147722e3a6a1e401fc440fd721c2d1aaf4fd0f94c4683b648f1249`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:11 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:11 GMT
ADD file:e2ae399c3aa36bf07b7d3562a21b9ad89f66ae6e03733ed0edcdcda5bd391c60 in / 
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:403b01240f845337685ead3abfb0228bb1d1b78b076d609aa20f4733d260f58f`  
		Last Modified: Wed, 30 Jul 2025 11:30:48 GMT  
		Size: 34.3 MB (34329650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d8efd726492aa10b73d11fd42a1886bd72b281cb65e022dc30839cff13805d`  
		Last Modified: Tue, 12 Aug 2025 22:53:02 GMT  
		Size: 199.9 MB (199874537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6c17105f29183404fb579fc2fdce6c10e43fe8e1e95ca1336f774a2e23758a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2360867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee42e66e283ca4a94e2db925a71eed5d192e33d7bd910fd513aa1288b4659f50`

```dockerfile
```

-	Layers:
	-	`sha256:5a9edbb44dcc16aa790bca3c3170ea5f50075abe435c93fccff16f0efb04e09f`  
		Last Modified: Wed, 13 Aug 2025 00:04:56 GMT  
		Size: 2.4 MB (2350522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e183dfe8e7e2ce2cc13de7f4130d1c5bb27625429b078d8e67d86389e93dcff`  
		Last Modified: Wed, 13 Aug 2025 00:04:57 GMT  
		Size: 10.3 KB (10345 bytes)  
		MIME: application/vnd.in-toto+json
