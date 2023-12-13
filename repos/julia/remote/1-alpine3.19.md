## `julia:1-alpine3.19`

```console
$ docker pull julia@sha256:040b969b7c57e3d2a442a51b00bdc5efc16784b1403861532161cf70ede60684
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1-alpine3.19` - linux; amd64

```console
$ docker pull julia@sha256:cb6584e6a83f62fb070e8d32ebc206a892116f9c392df9fabd152e40510bd830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154365991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d95bab7132a4f98113f3163d734ec22399d16bb7c6b38050c1027dc2c2968f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Sat, 09 Dec 2023 15:29:30 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 09 Dec 2023 15:29:30 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Dec 2023 15:29:30 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 09 Dec 2023 15:29:30 GMT
ENV JULIA_VERSION=1.9.4
# Sat, 09 Dec 2023 15:29:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.9/julia-1.9.4-musl-x86_64.tar.gz'; 			sha256='cfee0c02e470fd3e49a6d43b071ec905dec3a81d1ef377c0f0116f5b9920abe9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.9.4","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.9.4?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Sat, 09 Dec 2023 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 09 Dec 2023 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 09 Dec 2023 15:29:30 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b999a7a5f7902354baa34857ee26a2fda9b02e8b6b52e0b93ebb2f4073808b66`  
		Last Modified: Tue, 12 Dec 2023 20:50:18 GMT  
		Size: 151.0 MB (150957142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d1509eb900da2629572c716f284e464dcc6c0598155c32584eb14c38699045`  
		Last Modified: Tue, 12 Dec 2023 20:50:14 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-alpine3.19` - unknown; unknown

```console
$ docker pull julia@sha256:3d624eebc6fb4834a87e081d103df87b909802d225b4ea08d610be8d7d9da5e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 KB (82710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae22a042510ae944b644c5dad8b26a7943146f22e175cba01beff04d1c5fe327`

```dockerfile
```

-	Layers:
	-	`sha256:2901c91389348dc2384e2dcd3157e95f5cb5e979f57876cb5779876eb3962262`  
		Last Modified: Tue, 12 Dec 2023 20:50:14 GMT  
		Size: 68.0 KB (68037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9fc225418f85d14daaf8b59c02e628d492b30c792121826dd998ae1ba2dd046`  
		Last Modified: Tue, 12 Dec 2023 20:50:14 GMT  
		Size: 14.7 KB (14673 bytes)  
		MIME: application/vnd.in-toto+json
