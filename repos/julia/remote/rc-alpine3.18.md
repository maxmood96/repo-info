## `julia:rc-alpine3.18`

```console
$ docker pull julia@sha256:7c83ae829893870eef71e258fe04c3387f60ff1eaabd90ab4b1ea2ef0a49a32b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:rc-alpine3.18` - linux; amd64

```console
$ docker pull julia@sha256:fb1712d7ce4663ff4a582d01138056b2c2620150d21bb5af10bfe1afb4ccbe16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261116603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:987db3fe2a05395cee0bd0a812e45cc22883c54a2760fc4d1f5924f95310c5bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Wed, 10 Apr 2024 21:26:13 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 10 Apr 2024 21:26:13 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 21:26:13 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 10 Apr 2024 21:26:13 GMT
ENV JULIA_VERSION=1.11.0-beta1
# Wed, 10 Apr 2024 21:26:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.11/julia-1.11.0-beta1-musl-x86_64.tar.gz'; 			sha256='eee8f77c947b88334306ee4a9fce3633851a5d3954746138dc69e8be99b68b57'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.11.0-beta1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.11.0-beta1?os_name=alpine&os_version=3.18"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 10 Apr 2024 21:26:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Apr 2024 21:26:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Apr 2024 21:26:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51e5ccfb04ba51e5b532c47940ff12229eadcd2ae0dddfd03ae3a701478281e1`  
		Last Modified: Wed, 10 Apr 2024 23:56:50 GMT  
		Size: 257.7 MB (257713694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715531844398df3d7fa1261c1f9d5d97efc4a401c13370269b4ca05748d0fd04`  
		Last Modified: Wed, 10 Apr 2024 23:56:47 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-alpine3.18` - unknown; unknown

```console
$ docker pull julia@sha256:a2846d8876e4f9f4b0784d539b0b75f220272832e86b9fee4f686056a60126f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.6 KB (87558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce2db29f31ec6f872775ccdfa28dc3f05cdfb708971f809813bd06a569785795`

```dockerfile
```

-	Layers:
	-	`sha256:26ab436598fd749b7a0f33d7cc97821d0ff6a4a329aa44303ec137562f64579f`  
		Last Modified: Wed, 10 Apr 2024 23:56:47 GMT  
		Size: 74.3 KB (74283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e32a47049de29feca4ea8d666ed0e657faa11fdf69c744d6fa147fadfbf7c32`  
		Last Modified: Wed, 10 Apr 2024 23:56:47 GMT  
		Size: 13.3 KB (13275 bytes)  
		MIME: application/vnd.in-toto+json
