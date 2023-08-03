## `julia:rc-alpine3.17`

```console
$ docker pull julia@sha256:bb7c6a5788f145d7df2f9ad52cd80b78a54a12a46a57d1393b6b555c34d2e0ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:rc-alpine3.17` - linux; amd64

```console
$ docker pull julia@sha256:d142becae92fca8d7897d689804558dc6636c6a114dbd9a3780bc5321e71b7a0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.9 MB (172937066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90b865ae03b20f25be8abe9e089e3b2f6ff3c2a354d12c510eda1f4b9449943e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 14 Jun 2023 20:42:04 GMT
ADD file:828b07e74c184e7f251ed992ff195cdc50fdca345f13ff484e258851d928d950 in / 
# Wed, 14 Jun 2023 20:42:04 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 00:14:34 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 15 Jun 2023 00:14:34 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jun 2023 00:14:34 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 03 Aug 2023 00:30:59 GMT
ENV JULIA_VERSION=1.10.0-beta1
# Thu, 03 Aug 2023 00:31:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.0-beta1-musl-x86_64.tar.gz'; 			sha256='dfe4eb34da27e6bc8f036473b1765aa3e90d954a226a2c6b16c95f9081d94531'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Thu, 03 Aug 2023 00:31:17 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Thu, 03 Aug 2023 00:31:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Aug 2023 00:31:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4db1b89c0bd13344176ddce2d093b9da2ae58336823ffed2009a7ea4b62d2a95`  
		Last Modified: Wed, 14 Jun 2023 20:42:37 GMT  
		Size: 3.4 MB (3374713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8f3ed4a255abad16a218d707e577f37c4a9b2e1a23fa7f5161b6864c1911ac`  
		Last Modified: Thu, 03 Aug 2023 00:34:46 GMT  
		Size: 169.6 MB (169561980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6226dbb2ac0925e525e4d64a1c3499d5133d39848c156eb2da3cabed2446f91`  
		Last Modified: Thu, 03 Aug 2023 00:34:19 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
