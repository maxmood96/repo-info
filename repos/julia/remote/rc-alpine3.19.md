## `julia:rc-alpine3.19`

```console
$ docker pull julia@sha256:6a5f819832797d20ed7cc4fff92636273522114674fc37099a2f7917d50482dc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:rc-alpine3.19` - linux; amd64

```console
$ docker pull julia@sha256:50c4487790d94528ec876aff3261265592985f975e86ac404419d4f9d915b64a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.6 MB (254643139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2780402299e8a2172208b98c0cf56a919d0aa4d55448ed711f13f6338e6ff385`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Mon, 04 Mar 2024 21:21:28 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 04 Mar 2024 21:21:28 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Mar 2024 21:21:28 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 04 Mar 2024 21:21:28 GMT
ENV JULIA_VERSION=1.11.0-alpha1
# Mon, 04 Mar 2024 21:21:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.11/julia-1.11.0-alpha1-musl-x86_64.tar.gz'; 			sha256='955a2477ece891ed55b9f84d8cc4671221562bbfc7d4f90e75713ba73d9b482d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.11.0-alpha1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.11.0-alpha1?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Mon, 04 Mar 2024 21:21:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 Mar 2024 21:21:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 Mar 2024 21:21:28 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51eab44ac204d3bb6a96cb9c4c55aa62e6aa37049eafdd0b3dee74bf162fbd93`  
		Last Modified: Fri, 15 Mar 2024 23:55:28 GMT  
		Size: 251.2 MB (251234041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b258127f3f2f578e75e1aa72b101ee6a813e40cfee11f6b9d5860e4d2f2cb2ed`  
		Last Modified: Fri, 15 Mar 2024 23:55:21 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-alpine3.19` - unknown; unknown

```console
$ docker pull julia@sha256:4c8b897e46a57278086eae96bfb18b38177770fc663705867c1bdd9a7473e9b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.7 KB (139743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:230166fad3d307caaf322eb1159b6f71164b82fded64580a2ed8378f74cd4e2e`

```dockerfile
```

-	Layers:
	-	`sha256:b73f062874a9c3d6ba1e1c4a31ecf2fad372182db6715331cba131cfaa91111a`  
		Last Modified: Fri, 15 Mar 2024 23:55:21 GMT  
		Size: 125.5 KB (125516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dcc3d866f148b2557a6af1d09216b381b97c37092e8f8eb09159dacb221c3ec`  
		Last Modified: Fri, 15 Mar 2024 23:55:21 GMT  
		Size: 14.2 KB (14227 bytes)  
		MIME: application/vnd.in-toto+json
