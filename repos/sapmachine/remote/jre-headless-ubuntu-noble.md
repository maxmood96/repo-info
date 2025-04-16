## `sapmachine:jre-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:97eb93ed3da6765fe3b84a84d37e19b955a0bb36a89415cdae9f8d51314042e7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:2248fdd4d75d9cd4fa9579fb8bf7b656498351ac2141cc6ccc46dece9629971b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 MB (96603303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ef56cb0c56c004848aa03007dc7dd1a0e05660b89d95010ef10b16928121a1`
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
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff93da643e2c882eff405431108bddb9a63fa965fbfae5d9e4727b750f0ac2d`  
		Last Modified: Wed, 16 Apr 2025 16:13:40 GMT  
		Size: 66.9 MB (66885651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:27169fdaa416636cf26c82a8b377933e0fe0f9c63e79c15a384f2da29a358c3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2168639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683d4ac06dce04b3347a3930036d11e9bda22a88b0fd401d291fd35024d85ce4`

```dockerfile
```

-	Layers:
	-	`sha256:b340226ec7c87f843c881df71057afaf26bad8a2560666f218ebf39bf2c1c56c`  
		Last Modified: Wed, 16 Apr 2025 16:13:38 GMT  
		Size: 2.2 MB (2158012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b79e827ac3da8d66b073f655896860cf011fda590fcb2610a36ab6b2589fc9e`  
		Last Modified: Wed, 16 Apr 2025 16:13:38 GMT  
		Size: 10.6 KB (10627 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:b500752d7774d131d85ea2156ca0d66faa52419df80097c3d96eee230c1ff765
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94767282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6d0b082d4337483b446e26f83cb25bdc0a490fa5c48de803272714ce81c4e5a`
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
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5867ad48ec3eab7814eb8e583695c2f143c3a84944d2b4ee8d1d28a746d780a7`  
		Last Modified: Wed, 16 Apr 2025 16:16:20 GMT  
		Size: 65.9 MB (65920324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:bcce05db895fdafd88990fc2ebcf6759bd2fb2a4159d7eb78564ba54c1a15bd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2169319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16c56346982a6dc343962a66e5ac92ef71ab12db90016e74ac086bb1e0ac7407`

```dockerfile
```

-	Layers:
	-	`sha256:1978f2b6080bcbc75f4575b10c1eb85e835dad24f4d67b153c54a46028cafba5`  
		Last Modified: Wed, 16 Apr 2025 16:16:21 GMT  
		Size: 2.2 MB (2158528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a00366bfda12e76faff474d4275a5421a3c3c77ab25d43158cc6649156b0bce`  
		Last Modified: Wed, 16 Apr 2025 16:16:17 GMT  
		Size: 10.8 KB (10791 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:ee42c779f28935721ecc31c9a80ff9bb2a7ca0bddb47ce56c360d4bceb0da537
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102404840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f69e627baf457ca297a2b87ee66f9552efb410157c84d284995f766ae08eba8`
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
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7be894b3e11d60e6c310a10016f7c569f1a313b370ab3964114b1c135b1ce53c`  
		Last Modified: Tue, 08 Apr 2025 11:53:59 GMT  
		Size: 34.3 MB (34340867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f730e7ea7a95bde889c25d4bf73c98824b7241aaeff769453b865e8186bbd8b4`  
		Last Modified: Wed, 16 Apr 2025 16:20:54 GMT  
		Size: 68.1 MB (68063973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8880921762d350c5bba55d072baba174b414ac4c7c36318b92e51095c1af2b3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2171989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825549b1d112a24aaa25d2a3a3a4a365353f328225c693bcba10a7720beda619`

```dockerfile
```

-	Layers:
	-	`sha256:38eca0ed8759889fdb2304f68e0fc1be063b038ca3ea4ebadb729c49b4ef1cf2`  
		Last Modified: Wed, 16 Apr 2025 16:20:52 GMT  
		Size: 2.2 MB (2161288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7054d1954f6efcb64bb4dd87aed851bb3a883f7be4e2b4de7f94b1831501bb9`  
		Last Modified: Wed, 16 Apr 2025 16:20:51 GMT  
		Size: 10.7 KB (10701 bytes)  
		MIME: application/vnd.in-toto+json
