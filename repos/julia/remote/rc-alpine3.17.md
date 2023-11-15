## `julia:rc-alpine3.17`

```console
$ docker pull julia@sha256:ac890ec842d9d001b2f6c52eb6b41b97d7e2319c3d944923191462d55cd47b87
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:rc-alpine3.17` - linux; amd64

```console
$ docker pull julia@sha256:d386e5b2776542331e3beb56e1f55c9ba38318f9a6861c1bfd55792f10df154a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176300283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b687e0fd92e7bc223bb746c9270bb45af1a553316ef8ced74164d6a6001c8bfc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:26 GMT
ADD file:6dd87346b8be240b21b4f4d9296253bf0d28b6579aa52d2118872e3936963b6b in / 
# Mon, 07 Aug 2023 19:20:26 GMT
CMD ["/bin/sh"]
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 10 Nov 2023 15:26:46 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 10 Nov 2023 15:26:46 GMT
ENV JULIA_VERSION=1.10.0-rc1
# Fri, 10 Nov 2023 15:26:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.0-rc1-musl-x86_64.tar.gz'; 			sha256='07ca89f2a15db5e42a6e8d3325d093ddf7786ab2a4788ff9a5ad52bed40334c6'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0-rc1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0-rc1?os_name=alpine&os_version=3.17"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 15:26:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Nov 2023 15:26:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:9398808236ffac29e60c04ec906d8d409af7fa19dc57d8c65ad167e9c4967006`  
		Last Modified: Mon, 07 Aug 2023 19:21:08 GMT  
		Size: 3.4 MB (3378609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159817dff6a21c1ef772158c158fed005e460788ee952df69e1fe57e4adc341c`  
		Last Modified: Wed, 15 Nov 2023 02:22:07 GMT  
		Size: 172.9 MB (172921309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8bb64ba8ea93e5a6c243dd35527d4cccb88d4e8ed28f5b290a1a4f049173724`  
		Last Modified: Wed, 15 Nov 2023 02:22:03 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-alpine3.17` - unknown; unknown

```console
$ docker pull julia@sha256:3e5a495d8657be994cf904ec20ed744a37de52fa0ef1bb8cfb42edc3b5abef25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.8 KB (78760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc225aa59aa348cdc409dfd9d9d60acbad81ddaae0e7a38f8054eeeb2eb5e166`

```dockerfile
```

-	Layers:
	-	`sha256:2bdceca01fc6897816b05d02088d78c40fc48c85fd7ad85146b632c3118f04aa`  
		Last Modified: Wed, 15 Nov 2023 02:22:03 GMT  
		Size: 65.5 KB (65511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d3b1fd8f8551cedeb1f26aaa0b6fca3e803e3a03626fc667c617cde682aa113`  
		Last Modified: Wed, 15 Nov 2023 02:22:03 GMT  
		Size: 13.2 KB (13249 bytes)  
		MIME: application/vnd.in-toto+json
