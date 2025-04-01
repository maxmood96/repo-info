## `sapmachine:11-jre-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:47070cba603396b56d776021713cca88f014d71b4919f9d114a53a51d2b4a887
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jre-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:caf94cfbfcf4baeb6856058d6d8a2c521cb7dd0a1682da54c88df0525195d3d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80126110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70f45e8b3c19d4df080a4b520b398f51b35798e3a7ee7c65c5431a2471bea721`
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
# Mon, 27 Jan 2025 13:39:19 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 27 Jan 2025 13:39:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528b711767b363837e6a8eb6cc2aec6be1b2b947026ab98b2a0ac8767f5ba0a3`  
		Last Modified: Tue, 04 Feb 2025 04:50:18 GMT  
		Size: 50.4 MB (50371820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:337fb208e4b3fbd3b8c0486048cd9c7c868fe0928b76a2bd3414886a8496362b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2403258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7e748c02d0d4563fd7e1f9d20c6de4ff0de510b85ac8cdf516e24b86c637637`

```dockerfile
```

-	Layers:
	-	`sha256:693525b151809e83a6b13862a9f51d6b4ee4efe937926afbc2cbdfa1c6172ca0`  
		Last Modified: Tue, 04 Feb 2025 04:50:17 GMT  
		Size: 2.4 MB (2393787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bdc10f9a13a3bb5906d9820dc280381f09ba9a64448f612da5867f51b075a48`  
		Last Modified: Tue, 04 Feb 2025 04:50:17 GMT  
		Size: 9.5 KB (9471 bytes)  
		MIME: application/vnd.in-toto+json
