## `julia:rc-alpine`

```console
$ docker pull julia@sha256:b77bbac5bae9f3495a756634de28569ddba1fd5026bccca9b95bb9f406c81156
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:rc-alpine` - linux; amd64

```console
$ docker pull julia@sha256:b0b99e2ff80655b7bc91ec4b4ef449a36e4cc484d3600615608a2bc094ebf2ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.6 MB (258612579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dd0b2ce79500cac9030eda9b53c1ffe8b6129c63e3b6d7720452a3691c471f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
CMD ["/bin/sh"]
# Wed, 26 Jun 2024 17:59:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 26 Jun 2024 17:59:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jun 2024 17:59:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 26 Jun 2024 17:59:16 GMT
ENV JULIA_VERSION=1.11.0-rc1
# Wed, 26 Jun 2024 17:59:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.11/julia-1.11.0-rc1-musl-x86_64.tar.gz'; 			sha256='ffebb0734c274c7f66e3b07d428869f731bf617a76d89aa7f1afa94808f7a1a0'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Wed, 26 Jun 2024 17:59:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Jun 2024 17:59:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Jun 2024 17:59:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf786da2a469dafe4117b6f60cd9055c6f9704be7a1c5cc6e0d1bfa0b264cc2`  
		Last Modified: Thu, 27 Jun 2024 00:00:21 GMT  
		Size: 255.0 MB (254988365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af1a3862bb4ce142607ccfd48c99866c87caa560b9da5b4728c691794ab2898`  
		Last Modified: Thu, 27 Jun 2024 00:00:18 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-alpine` - unknown; unknown

```console
$ docker pull julia@sha256:c8ce866a7cf15461bf84e49ff14cb5b6e61d96041568612bd82dbcef2ecfa8bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 KB (83913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fde16eeb90d68a9673f15e14325d0483a290f1caca5641687c554b5a7d878eb`

```dockerfile
```

-	Layers:
	-	`sha256:8c4356ff2feb9dcd5aabd3ed6f88b6bbae42efc7bcae779313de2b2067fb3c14`  
		Last Modified: Thu, 27 Jun 2024 00:00:18 GMT  
		Size: 70.9 KB (70899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f1697fcfbc4857199d17a6690d6e1b2e1f5a97a5e4b5129a29eda938783a640`  
		Last Modified: Thu, 27 Jun 2024 00:00:18 GMT  
		Size: 13.0 KB (13014 bytes)  
		MIME: application/vnd.in-toto+json
