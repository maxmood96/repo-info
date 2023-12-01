## `julia:1-alpine3.17`

```console
$ docker pull julia@sha256:452c9d931deb20c468596ab6a7a164eaca94b788b2c569117292397a4343e51e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1-alpine3.17` - linux; amd64

```console
$ docker pull julia@sha256:5b3be18b25cb9c2875ed781fec0454ace9b4c801e4039f0e0a3691f1a7b7b032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.3 MB (154336997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88b622794bd77d670664a791b08a028426b72f0822ca6822402866d6e04d9d47`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 14 Nov 2023 18:59:25 GMT
ADD file:80331a5d882ac8a70763f4b19e06f2e04ea3dca34ae6d92810815b170b3c806c in / 
# Tue, 14 Nov 2023 18:59:25 GMT
CMD ["/bin/sh"]
# Tue, 14 Nov 2023 18:59:25 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 14 Nov 2023 18:59:25 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Nov 2023 18:59:25 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 14 Nov 2023 18:59:25 GMT
ENV JULIA_VERSION=1.9.4
# Tue, 14 Nov 2023 18:59:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.9/julia-1.9.4-musl-x86_64.tar.gz'; 			sha256='cfee0c02e470fd3e49a6d43b071ec905dec3a81d1ef377c0f0116f5b9920abe9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.9.4","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.9.4?os_name=alpine&os_version=3.17"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Tue, 14 Nov 2023 18:59:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 18:59:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 18:59:25 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1207c741d8c9b028d98c4006013f9de959da3c55f85b91ed5e4583438a0112ca`  
		Last Modified: Thu, 30 Nov 2023 23:23:40 GMT  
		Size: 3.4 MB (3379323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48287cac50ff66d53e8ef6467e3f3149eb9cf8176504cacb58a7f01d8537f9a`  
		Last Modified: Fri, 01 Dec 2023 00:11:06 GMT  
		Size: 151.0 MB (150957305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e9ecdfc60e43370d3189b6834a379d65276aab081e0cb7dfd1d3d12cf33851`  
		Last Modified: Fri, 01 Dec 2023 00:11:02 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-alpine3.17` - unknown; unknown

```console
$ docker pull julia@sha256:6354e0f56d15647af0215b2aa2c9f4cdfaac621afccc7ac08fb67e012d2f6f50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 KB (79251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c379ff5a0e1cac66b5d53b9fac8598ed355fcc8f4b192085f50bb7551ee1ad1`

```dockerfile
```

-	Layers:
	-	`sha256:c3c3cfdf49eb846381e17a8f8c6b0f068966bd79970ac159dead0b30909257d0`  
		Last Modified: Fri, 01 Dec 2023 00:11:03 GMT  
		Size: 65.8 KB (65785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47e2a2fe352ef3ffc771d93a5d849ef83d3996f99744961d21026b6f1f06e85e`  
		Last Modified: Fri, 01 Dec 2023 00:11:03 GMT  
		Size: 13.5 KB (13466 bytes)  
		MIME: application/vnd.in-toto+json
