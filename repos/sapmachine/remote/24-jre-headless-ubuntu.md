## `sapmachine:24-jre-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:644f642293fef91653b035d535820caa1d962f69c8010d33ea7ca1c077f66b46
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:24-jre-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:bcf40838fe095f29d2b1fa681eca16a01dbae00e9e07a145315930906e91be6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 MB (96603320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:859b7888da6e9da07d105a9129cb786c964718ab7b9d3ca8e8624701b03049ee`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2007461a5f79a2e070d9b28128fc5c8b2f69a029fcb6d4078bb0add74b6531c`  
		Last Modified: Mon, 05 May 2025 16:36:50 GMT  
		Size: 66.9 MB (66885791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b0d80f8e7658b582c879ab2d19539314ed09d2bc17976625b62f3356d5dcaa24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2168643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd24ba03b2f6ca938732fbebc316567c56a514a4a1467ff312e6121c1177a843`

```dockerfile
```

-	Layers:
	-	`sha256:29fdd547d660c15bed60a5f33a9b0478391aeaccdfa26b326d5826405a97a8a6`  
		Last Modified: Mon, 05 May 2025 16:36:48 GMT  
		Size: 2.2 MB (2158016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4d5f7c22370b04e5d5c255bfa3e27324d773453d54e4ed46bc7a744ad9571a4`  
		Last Modified: Mon, 05 May 2025 16:36:48 GMT  
		Size: 10.6 KB (10627 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jre-headless-ubuntu` - linux; arm64 variant v8

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

### `sapmachine:24-jre-headless-ubuntu` - unknown; unknown

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

### `sapmachine:24-jre-headless-ubuntu` - linux; ppc64le

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

### `sapmachine:24-jre-headless-ubuntu` - unknown; unknown

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
