## `julia:alpine3.21`

```console
$ docker pull julia@sha256:fa393b467e0644687f2280e6c157055cc9554a620a78e2606a93484414a20932
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:alpine3.21` - linux; amd64

```console
$ docker pull julia@sha256:9b3c67dfd9667cef43d3cb4aeb988c17aa6ab0fa8b4eb7723a353d6a8279ebcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294455526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e9d5d439ee39885b3f676e9ebbfc8c1095d2ecd20da5c82180cec159b8f5d9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 14 Apr 2025 23:59:20 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 14 Apr 2025 23:59:20 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 23:59:20 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 14 Apr 2025 23:59:20 GMT
ENV JULIA_VERSION=1.11.5
# Mon, 14 Apr 2025 23:59:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.11/julia-1.11.5-musl-x86_64.tar.gz'; 			sha256='1a5ff1dabf9c712502d17ea38bc9aa5507ae3e6f6add438fa34b77a3df8e466c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Mon, 14 Apr 2025 23:59:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 23:59:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 23:59:20 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea434ae7341ef9c46946ce48ed3e82829df7b3e399092ee9b32c27e198f51808`  
		Last Modified: Thu, 08 May 2025 19:43:45 GMT  
		Size: 290.8 MB (290812912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6b8bee427e8a8fca3727afd82cc11a38ba0131ec19fc915884654a12965858`  
		Last Modified: Thu, 08 May 2025 19:43:29 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:alpine3.21` - unknown; unknown

```console
$ docker pull julia@sha256:4a122c603e89f9bf6cf85a117fe5fea0148ebcd51053053bd881ff328d996bcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 KB (93652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c408505422821c128d4ebc99ef8c018796f3f5494966e0771781418dd4063c60`

```dockerfile
```

-	Layers:
	-	`sha256:ed8ba6a29d44067d2e54ff2778faa55ede534fab2a3325837af589e80318fb47`  
		Last Modified: Tue, 15 Apr 2025 21:52:49 GMT  
		Size: 79.9 KB (79864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24af34bc1f2f0e32ab91111730e85752efdd12c6a345b813ee112eea57bcb00e`  
		Last Modified: Tue, 15 Apr 2025 21:52:49 GMT  
		Size: 13.8 KB (13788 bytes)  
		MIME: application/vnd.in-toto+json
