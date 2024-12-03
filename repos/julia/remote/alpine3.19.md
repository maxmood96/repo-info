## `julia:alpine3.19`

```console
$ docker pull julia@sha256:eaaa257792ae7bfbf757120697cc12e527004dc5b3ea9d4caee9e19e1f737cbf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:alpine3.19` - linux; amd64

```console
$ docker pull julia@sha256:53977ddbcdcac1829ef2809fa95ddf813b53618b4101f234021cd788b415759e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.3 MB (294252889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51e0779439b0d28fec6d61a4325ff7ea5312514a3e89ece27100a98e5b938171`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.11/julia-1.11.2-musl-x86_64.tar.gz'; 			sha256='dc7d2ec533c33f385683bad892d09c9f09f124061fa00ab7e4dd2e0912d55c19'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a672057c033e864fb813164b8d418021f328aa2fec4f32f7926a2ec7eed86f3`  
		Last Modified: Tue, 03 Dec 2024 15:35:20 GMT  
		Size: 290.8 MB (290832796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7da7c421026147a9b51a29fcd96a383eb2fe6319258ee4d5242b4bf9b20846f`  
		Last Modified: Tue, 03 Dec 2024 15:35:17 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:alpine3.19` - unknown; unknown

```console
$ docker pull julia@sha256:2e2ce7284282ee19516e4e8d6a0bc997c5792641fbe6b67fd048e552585d048f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 KB (89830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b0c636b45c5098c0b18cfdcf0da73985002ebf9464f586db8113954b9946962`

```dockerfile
```

-	Layers:
	-	`sha256:918737cdf23281c404781987f9597d6ca945a30915c9a63b8e6e5e24aea66967`  
		Last Modified: Tue, 03 Dec 2024 15:35:17 GMT  
		Size: 77.3 KB (77255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7847792b2aa61197a6b78218d4c4bfb21d87ca4e325e932f72516a5ecc8dfed3`  
		Last Modified: Tue, 03 Dec 2024 15:35:17 GMT  
		Size: 12.6 KB (12575 bytes)  
		MIME: application/vnd.in-toto+json
