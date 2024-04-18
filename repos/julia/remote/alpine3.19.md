## `julia:alpine3.19`

```console
$ docker pull julia@sha256:81349ee82fab634dab52fc21af7834f4dce9b67414f017b7fefd4adaec9f8914
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:alpine3.19` - linux; amd64

```console
$ docker pull julia@sha256:5ce4ad440b9c73dc11481ef4855478413d242ba0f88e55ce315d9545c6d31147
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.4 MB (176433078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4456df6c15211b39c2165380e9b9ef0fe04e3899574bf930039dabb1144c786f`
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
	-	`sha256:8fa1f7e53fc4bc45ba6e40e73ef83f7c7abb16cbbbfdbbcada0d46408840569a`  
		Last Modified: Fri, 15 Mar 2024 23:54:47 GMT  
		Size: 173.0 MB (173023985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d351c286db530cda2e451cd24287aff6c8aff6405958cc35233d1516bb1d139`  
		Last Modified: Fri, 15 Mar 2024 23:54:43 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:alpine3.19` - unknown; unknown

```console
$ docker pull julia@sha256:383bf2eccf8fef81477d905bf29c979c426a16cfda10440b2d043b097de1b35e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.9 KB (128881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ce2c2c9f6abde8435a6ade6aa47e1b9f36a7f8bb6dbf79adaf88142fa596a88`

```dockerfile
```

-	Layers:
	-	`sha256:1502a25bd9d864b1e5e55a40956d06f448e08c290879a58fd4bd8c0e2889c22b`  
		Last Modified: Fri, 15 Mar 2024 23:54:44 GMT  
		Size: 114.2 KB (114184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fa1ef566117093a1388186b482ecc687d961edd34cc6c54245c976e8d6fdee3`  
		Last Modified: Fri, 15 Mar 2024 23:54:43 GMT  
		Size: 14.7 KB (14697 bytes)  
		MIME: application/vnd.in-toto+json
