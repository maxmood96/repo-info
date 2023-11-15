## `julia:alpine`

```console
$ docker pull julia@sha256:7b94bd6e95fbcaa45704b950b31205e57cdf2043e64d35c09696acd9746d257e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:alpine` - linux; amd64

```console
$ docker pull julia@sha256:78b94bed175f3b035aaeed1682d7579f85d9b25daa4fb74d2ea8c2f5b5139e20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154359512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81ef656e88e98a8bcc89d56878f04de3e7a319bd4eca3df002981f67535b8c10`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
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
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.9/julia-1.9.4-musl-x86_64.tar.gz'; 			sha256='cfee0c02e470fd3e49a6d43b071ec905dec3a81d1ef377c0f0116f5b9920abe9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.9.4","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.9.4?os_name=alpine&os_version=3.18"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Tue, 14 Nov 2023 18:59:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 18:59:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 18:59:25 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5291effa2e94d7453499090779d97df95e976141128ac5f999f85c38c2fdf2`  
		Last Modified: Wed, 15 Nov 2023 02:22:06 GMT  
		Size: 151.0 MB (150957176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935096cdba8dc3b9b7937ebf0c4471af8c97b77bfc81db8ddce858a722468662`  
		Last Modified: Wed, 15 Nov 2023 02:22:04 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:alpine` - unknown; unknown

```console
$ docker pull julia@sha256:c142af057e355fff05f829ae1334b282d1a820d47fcca096074da164e67a73fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.2 KB (82163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d4dfdc2c2233c9221b6b39ae5dc005c520fdba4b2fe7f6ba091e1cbd4777d13`

```dockerfile
```

-	Layers:
	-	`sha256:211bc3d5fa72f86c76090f440c7959afb0fe831c0470e3c9f14ed87ff7c30e91`  
		Last Modified: Wed, 15 Nov 2023 02:22:04 GMT  
		Size: 67.5 KB (67489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:951234097f99bb7ba173aea38e4ae75486d45e498e0d7fd332e38f976e29eec2`  
		Last Modified: Wed, 15 Nov 2023 02:22:04 GMT  
		Size: 14.7 KB (14674 bytes)  
		MIME: application/vnd.in-toto+json
