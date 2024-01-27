## `julia:alpine3.18`

```console
$ docker pull julia@sha256:77a977b5edcfe0878250b81503abbe31f1425e64a0f12e1ada4d51b1da34758c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:alpine3.18` - linux; amd64

```console
$ docker pull julia@sha256:5299d783ae55d8ef632b9cc263458d66a810a4de77a03ffae4e7fa820264aa53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176676774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee49bd257b2df90a18d0154e828326a5fcba99b347173d2169fe13bcd43dff0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["/bin/sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.0-musl-x86_64.tar.gz'; 			sha256='da8a9e0cf31eddd776276321802b9744acf5b8ce0171854b3e9d6394f656f9a2'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=alpine&os_version=3.18"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5204fc615595fd1ad835b0750c5fdb927818512d88052aef7e3850c09dd45475`  
		Last Modified: Sat, 27 Jan 2024 00:53:33 GMT  
		Size: 173.3 MB (173273866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3bd7244621863d2bbcbbe233abec587e6b376a86cab3eaec7803f2556e535f`  
		Last Modified: Sat, 27 Jan 2024 00:53:29 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:alpine3.18` - unknown; unknown

```console
$ docker pull julia@sha256:da0ca027e598e9773b125a066c844f5cefc1ecbbfb387e5b7661abd53bd31fe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 KB (80746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c093cd0eedbfc6980a82434ffc3879914906fc76b8f084df18d5c9012ffdb2aa`

```dockerfile
```

-	Layers:
	-	`sha256:58ec49d3d0285541a48ea975d3b7fdda895fc33f2c2d93c8933a42c1a3651f1a`  
		Last Modified: Sat, 27 Jan 2024 00:53:29 GMT  
		Size: 67.3 KB (67260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:187a1d23ed3a8d36572659404c674c1615b777fd9041abe5246a10eb10691ae7`  
		Last Modified: Sat, 27 Jan 2024 00:53:29 GMT  
		Size: 13.5 KB (13486 bytes)  
		MIME: application/vnd.in-toto+json
