## `julia:rc-alpine3.18`

```console
$ docker pull julia@sha256:feee1b2ea3c51dd0b00c944a66d0161062a083070f1cb85ccdfb4d1c43070894
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:rc-alpine3.18` - linux; amd64

```console
$ docker pull julia@sha256:47d02db9c3b6b4ec225258719a010e2699747e9c3351c7c72f62830a27d6d6cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.5 MB (176511761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a37f8713f841171ea83fbcd3d041c688f745648c96e04d799a32b9889c7d7c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Mon, 04 Dec 2023 00:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 04 Dec 2023 00:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Dec 2023 00:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 04 Dec 2023 00:59:15 GMT
ENV JULIA_VERSION=1.10.0-rc2
# Mon, 04 Dec 2023 00:59:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.0-rc2-musl-x86_64.tar.gz'; 			sha256='65aa6d1a09e1ea376f7e351c80def41c077b63c15035cb118c6ad17e7870f6fe'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0-rc2","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0-rc2?os_name=alpine&os_version=3.18"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Mon, 04 Dec 2023 00:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 Dec 2023 00:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 Dec 2023 00:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de325b4cafd23372197f1dfaeb2742f080631fa681731b5bb742c08c6f4ca710`  
		Last Modified: Tue, 05 Dec 2023 01:12:36 GMT  
		Size: 173.1 MB (173108974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00005cf40ef19adfd45a05007c573905629b13e8d76e1bb3ce4977daa812c47`  
		Last Modified: Tue, 05 Dec 2023 01:12:33 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-alpine3.18` - unknown; unknown

```console
$ docker pull julia@sha256:afa2c6fd74c84bbfae57eaea501ca6fab7563caac98fa37c7edc1a44d19f42f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.1 KB (81122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:180adad6d7300748fce72c72dd284c0b4189294667b8c72278ee00b2d8c10d62`

```dockerfile
```

-	Layers:
	-	`sha256:54869b7e87f588a3c8812a7c48ebe952eceda36112182d1052cf29a6e3268088`  
		Last Modified: Tue, 05 Dec 2023 01:12:34 GMT  
		Size: 66.9 KB (66939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae768b91cf988590f6d1a4792ffa14a197453e6c2c74b540c295a8319c757fd0`  
		Last Modified: Tue, 05 Dec 2023 01:12:34 GMT  
		Size: 14.2 KB (14183 bytes)  
		MIME: application/vnd.in-toto+json
