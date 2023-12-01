## `julia:rc-alpine3.17`

```console
$ docker pull julia@sha256:9444c3fb4211ae57f9d111ad721134d63e7a0e424516fd75bae1955421c18c49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:rc-alpine3.17` - linux; amd64

```console
$ docker pull julia@sha256:76cc6937e00cc947c1636f3af4e063ac22e090aac24b9005c5f18b3fd9e9469e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176301317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a0fa3e092a840ee786686788a71e75d162d4bf9b21adb0249b1b11519ad20e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 10 Nov 2023 15:26:46 GMT
ADD file:80331a5d882ac8a70763f4b19e06f2e04ea3dca34ae6d92810815b170b3c806c in / 
# Fri, 10 Nov 2023 15:26:46 GMT
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
	-	`sha256:1207c741d8c9b028d98c4006013f9de959da3c55f85b91ed5e4583438a0112ca`  
		Last Modified: Thu, 30 Nov 2023 23:23:40 GMT  
		Size: 3.4 MB (3379323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28f9869525638f3b9bf79ad1f751d2548e0f2a4631dfc63e06b5b339367d2db`  
		Last Modified: Fri, 01 Dec 2023 00:11:09 GMT  
		Size: 172.9 MB (172921627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12579fd6e4429924391dd0120918958373526cdab7fb143b0e306a815586875`  
		Last Modified: Fri, 01 Dec 2023 00:11:06 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-alpine3.17` - unknown; unknown

```console
$ docker pull julia@sha256:460dc8c6a4980b4a9d245d63e2541d42caeed3fdfe3f40aafe152a9f5c22031e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.8 KB (78762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc3bba646554b52b0efe0d0ad8b11e6ea3711ffa0ddb244193567ace86f10db2`

```dockerfile
```

-	Layers:
	-	`sha256:1faeecf151ef2141177b4e44b52ee7853e07499b312c17ea5b00369a99623d24`  
		Last Modified: Fri, 01 Dec 2023 00:11:06 GMT  
		Size: 65.5 KB (65511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b1b02f4af6ab8e53444bbee0cfbc2a26889a57adabfe8ac440275a461c55978`  
		Last Modified: Fri, 01 Dec 2023 00:11:06 GMT  
		Size: 13.3 KB (13251 bytes)  
		MIME: application/vnd.in-toto+json
