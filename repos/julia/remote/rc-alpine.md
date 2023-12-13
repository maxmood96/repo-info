## `julia:rc-alpine`

```console
$ docker pull julia@sha256:27b3a5112bb6b45f986930eb8e470fc8d528350b30d455e49cf03948cfc0819b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:rc-alpine` - linux; amd64

```console
$ docker pull julia@sha256:c50f85b19607512da589ce58a499d6724470c8a8a047a9ef2acec17accdb8349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.5 MB (176518816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b35d774df66c570c629d90c6ea5762a493e78da481de17435ac09e9e219b6a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Sat, 09 Dec 2023 15:29:30 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 09 Dec 2023 15:29:30 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Dec 2023 15:29:30 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 09 Dec 2023 15:29:30 GMT
ENV JULIA_VERSION=1.10.0-rc2
# Sat, 09 Dec 2023 15:29:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.0-rc2-musl-x86_64.tar.gz'; 			sha256='65aa6d1a09e1ea376f7e351c80def41c077b63c15035cb118c6ad17e7870f6fe'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0-rc2","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0-rc2?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Sat, 09 Dec 2023 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 09 Dec 2023 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 09 Dec 2023 15:29:30 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff16fedd82d4429175f117be071826588cd9cced6676cec37ff76ccdb2f6916c`  
		Last Modified: Tue, 12 Dec 2023 20:50:21 GMT  
		Size: 173.1 MB (173109968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a60ea883b388c17d3d5185ca2b278c6c18b752afdd2f66b5c78f64bd04b7e4`  
		Last Modified: Tue, 12 Dec 2023 20:50:17 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-alpine` - unknown; unknown

```console
$ docker pull julia@sha256:f1ced58d72a058bcf7b0f25b2ee3633d451558bb11ebcea5878bc03255fd370e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 KB (81670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6666e4b59503754ecec6e8cb2bf2cbfe8e71b9bfd00ec68a0d93c7cb23693bd7`

```dockerfile
```

-	Layers:
	-	`sha256:f55386bf17b47be48aa3a9f23a65a94d470fd03393f5ea6865f75571f226b37e`  
		Last Modified: Tue, 12 Dec 2023 20:50:17 GMT  
		Size: 67.5 KB (67487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94aa64b5fe927fd70a245db9e70ebfb5217b44372ec2a4eee4744c4ac2067231`  
		Last Modified: Tue, 12 Dec 2023 20:50:17 GMT  
		Size: 14.2 KB (14183 bytes)  
		MIME: application/vnd.in-toto+json
