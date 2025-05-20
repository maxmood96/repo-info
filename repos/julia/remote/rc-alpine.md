## `julia:rc-alpine`

```console
$ docker pull julia@sha256:16603705f0937b4b5b33a9f5772f12a16376ba986a83691cb5ad7b78fb300eb9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:rc-alpine` - linux; amd64

```console
$ docker pull julia@sha256:9028d349d99ca3804c73c4f13f95b22e85a32a3a3ab5076c6c5e2015266b481e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.8 MB (300786775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe088d49d2a544b3619900daf05f58e0116f382e388e95161711103f6ec85152`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 23:59:27 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 12 May 2025 23:59:27 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 May 2025 23:59:27 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 12 May 2025 23:59:27 GMT
ENV JULIA_VERSION=1.12.0-beta3
# Mon, 12 May 2025 23:59:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.12/julia-1.12.0-beta3-musl-x86_64.tar.gz'; 			sha256='4db9ef34463798fdeaff91c7cf4b8880b3bd135e2e809aae934bab6f2cba8d33'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Mon, 12 May 2025 23:59:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 12 May 2025 23:59:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 May 2025 23:59:27 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b73e2e1365b614b904486ed24ed20a18b090d60b08be72a9a04dbee4d7c2b56`  
		Last Modified: Tue, 13 May 2025 19:58:45 GMT  
		Size: 297.1 MB (297144160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce921a4710db7b3d7da4249b5f2c1dbe0b42624d3f5f2397bdfdc79a8aa434e`  
		Last Modified: Tue, 13 May 2025 19:58:39 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-alpine` - unknown; unknown

```console
$ docker pull julia@sha256:a5ef32e6cd59ad5a50265ea34e617216dc89ba5618371c3bd7134d3954342a7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 KB (92577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b7f405303476d9a6b2f5b226b029c34392eec63ca2be369f3e7c59bd60a286`

```dockerfile
```

-	Layers:
	-	`sha256:0bfe6acc6417fffb8e93579b9dd880a6a8ffb5d9fbb7c6609e7dbe6bc5981f0b`  
		Last Modified: Tue, 13 May 2025 19:58:39 GMT  
		Size: 79.3 KB (79304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:528d3490810e65ad51db9e4852ac3b9adf11db0d871ec74624d048514e7d61ba`  
		Last Modified: Tue, 13 May 2025 19:58:39 GMT  
		Size: 13.3 KB (13273 bytes)  
		MIME: application/vnd.in-toto+json
