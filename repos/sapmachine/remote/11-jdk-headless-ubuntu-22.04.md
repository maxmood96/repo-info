## `sapmachine:11-jdk-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:464c3fb18309e89ca2c0e9d642bc52fe6144fab133d5d3fd2819dee8b04c273e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jdk-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:ad7b588aa53c02f87edbc3bdf680f56545e29c2fc1348a6072f4b252e2f10446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.6 MB (228574295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed26bbb06e7284acbeb0749d61d33622f201cc9650016a83c599794b6ba5ac58`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:47:31 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.29 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:47:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 15 Jan 2026 22:47:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0998afc6b445e9f133c02062cbfb2def086683b95ca1701d07335c17d6449c`  
		Last Modified: Thu, 15 Jan 2026 22:48:26 GMT  
		Size: 199.0 MB (199037628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:78df30ed73e854d85e40e9a6f10d1b01620679b47fdfd37e41f2281cb6a9c806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2397409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c533ac7bc9669dd2a4b20504820cb8f83aa0d5c3fb7c61e8747341c3337d469f`

```dockerfile
```

-	Layers:
	-	`sha256:a1b2aa6f343ee1ec6cabadebd45f8743055365f6e376d11d57ec82f565abc056`  
		Last Modified: Thu, 15 Jan 2026 22:47:49 GMT  
		Size: 2.4 MB (2388519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29f0f4d0bc48179ecbb2fbba2b94d7fcefb2a122b61cbd3b1d818efaffe10ac7`  
		Last Modified: Thu, 15 Jan 2026 22:47:48 GMT  
		Size: 8.9 KB (8890 bytes)  
		MIME: application/vnd.in-toto+json
