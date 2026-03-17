## `sapmachine:11-jre-headless`

```console
$ docker pull sapmachine@sha256:d110345f318b7394d9cb16e0f2323a0ebd0334364ab4b7ef866b07f079bef66c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jre-headless` - linux; amd64

```console
$ docker pull sapmachine@sha256:6798d326c34da2beff6d31ffa661c3c02ec46da9e234113ea0cb0d939265c692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78635725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e334fc1922435797542c511bb97d15271751ffef6a8f53996531f74bc12f0788`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:25:57 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.30 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:25:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Tue, 17 Mar 2026 02:25:57 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48bc58e1549eef6536a665cb350dc61ec9e31fdaea3269f50dbcfbdbfc2a0b5b`  
		Last Modified: Tue, 17 Mar 2026 02:26:08 GMT  
		Size: 48.9 MB (48903732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3b69f53ea5bd78544de601a9308878e74cc0385aa90361ccee190389511b1f71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2288092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9df55901d5729753ac1aa164e772a6837c71dd42afa0b53d7d3bfd468b60523`

```dockerfile
```

-	Layers:
	-	`sha256:8d662e7a8fe722c0f54d783ab55b2f5b6dafab965cec54233567632c7fef659e`  
		Last Modified: Tue, 17 Mar 2026 02:26:07 GMT  
		Size: 2.3 MB (2277863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71ac9e848d5fa3e63daed3a63b6589f16642f0fd40b49478804ba73c83c31836`  
		Last Modified: Tue, 17 Mar 2026 02:26:07 GMT  
		Size: 10.2 KB (10229 bytes)  
		MIME: application/vnd.in-toto+json
