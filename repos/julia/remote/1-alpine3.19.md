## `julia:1-alpine3.19`

```console
$ docker pull julia@sha256:fbce10e9193cb5922ba19d28d06da5c716aeff903cac478f458b912e9ce3dafa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1-alpine3.19` - linux; amd64

```console
$ docker pull julia@sha256:c414c068f0774b44cc122569bb6cd211537d6781ee2249c018d844646253b4bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.4 MB (176433162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:319a2f71d4f99d58f100c66506adc3d1a3af64e5da98e6def8ea0cd37ed1a03c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 02 Mar 2024 06:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 02 Mar 2024 06:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Mar 2024 06:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 02 Mar 2024 06:59:15 GMT
ENV JULIA_VERSION=1.10.2
# Sat, 02 Mar 2024 06:59:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.2-musl-x86_64.tar.gz'; 			sha256='c5fe3500154e73a44cc09e4d4a40ffe4374b8914c82e5c1ccde44d36feb6f5e6'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.2","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.2?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Sat, 02 Mar 2024 06:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 02 Mar 2024 06:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 02 Mar 2024 06:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f9be1d9386814e37474165b828692649103e4809a589f420ebd2ba71d390176`  
		Last Modified: Tue, 05 Mar 2024 00:50:01 GMT  
		Size: 173.0 MB (173024065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df3843646a1dc870c2a444d6438937ea29166bbfd1d11a4cfc6eaf761cb469d`  
		Last Modified: Tue, 05 Mar 2024 00:49:58 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-alpine3.19` - unknown; unknown

```console
$ docker pull julia@sha256:b7227179329a71c2841db801281ab9d72876997f60be327e610a887a2ef22f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 KB (127871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c42639af54a4aeeafc5f4fc4d9644075bd7cf396f6a815dd98ea7798ec67f6cd`

```dockerfile
```

-	Layers:
	-	`sha256:e8f0571ed1e91fe2c865d71450a60af6b4fc5eb4e59e64ad594f69b2cc23636d`  
		Last Modified: Tue, 05 Mar 2024 00:49:58 GMT  
		Size: 113.2 KB (113173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6805d50f2f1b6d27fdede8429904c9354ce1daad45c0b2021c7a72261bcc2a8a`  
		Last Modified: Tue, 05 Mar 2024 00:49:58 GMT  
		Size: 14.7 KB (14698 bytes)  
		MIME: application/vnd.in-toto+json
