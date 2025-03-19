## `sapmachine:24-jdk-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:bf22036285b725aabded3c6414750b9e918fb29ac159b1deb6bcf963a3fc6d0a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:24-jdk-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:effc750fa34d5416f1e5c1376b17ad1f608ee63479555a1d05354405906ac0df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.5 MB (264549986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fa41f5966ee8a970cb78c639c2fe90a40bc476152c7a6fd701689a359a96d84`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7344b24cfd52d5b7ab4991dfb0891ef569e7bed04198d7d139ef5badc36752f`  
		Last Modified: Wed, 19 Mar 2025 20:33:16 GMT  
		Size: 234.8 MB (234795696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jdk-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a76e42f53241ceaed8304b66de3326e32526b9bdefaf18edb80a9e969f2ef34f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2476389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94712b8cb3e08c34a7afbcdf6edbfd22e8e46f095fd2ea372e8b2908abd9bdb6`

```dockerfile
```

-	Layers:
	-	`sha256:9521d6ba93a99fbf59c9bca5448e76ae458cac1aa3270b9f8fd6cc164c57fa35`  
		Last Modified: Wed, 19 Mar 2025 20:33:12 GMT  
		Size: 2.5 MB (2465090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7795fc2fbb652cd1a42516a10c734952b09fb8346fad99be036af6332bdbb9ab`  
		Last Modified: Wed, 19 Mar 2025 20:33:12 GMT  
		Size: 11.3 KB (11299 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jdk-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:ba3f28f117dab887c19dcc2fbd491453b8bf5a78368555df28b4e1cb74148b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261450526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e33f2431c2e82fdc3c122b32604acaa001e91fefa037687ab1998ed1e680e224`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11c53936a49f11dab09db667c9f6380067a86be449f9ece0bfd550a497645a5`  
		Last Modified: Wed, 19 Mar 2025 20:33:03 GMT  
		Size: 232.6 MB (232556928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jdk-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:161c3e80499d7f4810297575161d98f5d4ee6bc929c7f4837fe81fc7348bb563
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2477150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53dafccadc2274374c4eb618315203f12026f14fdb0d34bae3c12dc9dcb046bc`

```dockerfile
```

-	Layers:
	-	`sha256:f3922ea2aafee2e27b5a93887cc781832a71baa2013fabc6e2429a661d2adeba`  
		Last Modified: Wed, 19 Mar 2025 20:32:58 GMT  
		Size: 2.5 MB (2465651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86a7334f1d276c0522945cde43156eadddd7361ac38c6b543408bf2202d6b6f9`  
		Last Modified: Wed, 19 Mar 2025 20:32:58 GMT  
		Size: 11.5 KB (11499 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jdk-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:9c2c335328d12c4003a5d211dc8ac54e6499879c695f17fb8e4dda2193838223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270744617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74b12d73d4c24e139667745ea5a679befb59efb753e74a7b654ffdbe9588e2c6`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:16:03 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:16:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:16:07 GMT
ADD file:8c71b040cc97f9d076a34d57cd957e6b33cdfb8f115e1ba283b674e6aad793d8 in / 
# Mon, 27 Jan 2025 04:16:07 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Mon, 27 Jan 2025 05:10:08 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc072e12332c0a15a48df463ab8a66387f98a818ea4476acc9b836b98ab4aeae`  
		Last Modified: Wed, 19 Mar 2025 20:34:01 GMT  
		Size: 236.4 MB (236354793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jdk-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0f6c9c265fae11343b082b44ae61af30f74cd1a1a2c746e382d8b87de04c522f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2477904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ab2ac9f553fdb6d018695a640649073cc82b7ed13ceb49b36da5139ae50862`

```dockerfile
```

-	Layers:
	-	`sha256:befa1f8a996a076830abf094b8479f1b7fdbf0caabf46de6485002190d805129`  
		Last Modified: Wed, 19 Mar 2025 20:33:53 GMT  
		Size: 2.5 MB (2466513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce8727040141704a9f06f17e5580ac243fd9517bf1593d263b8771a76ff255a9`  
		Last Modified: Wed, 19 Mar 2025 20:33:52 GMT  
		Size: 11.4 KB (11391 bytes)  
		MIME: application/vnd.in-toto+json
