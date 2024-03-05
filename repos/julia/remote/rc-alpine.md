## `julia:rc-alpine`

```console
$ docker pull julia@sha256:3acd34ebaf41ddd0f06cf5b299166676b3353b69beffc907cdc21db586a249ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:rc-alpine` - linux; amd64

```console
$ docker pull julia@sha256:c71b1bf4ab7181f9e708ea6bd556ca379cfaa4a9c3ca857b52c60c099ec9283b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.6 MB (254643106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f64202039a4279eae06150f99fa986e70e3a89b009fa84c2c257c3010969148`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Mon, 04 Mar 2024 21:21:28 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 04 Mar 2024 21:21:28 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Mar 2024 21:21:28 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 04 Mar 2024 21:21:28 GMT
ENV JULIA_VERSION=1.11.0-alpha1
# Mon, 04 Mar 2024 21:21:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.11/julia-1.11.0-alpha1-musl-x86_64.tar.gz'; 			sha256='955a2477ece891ed55b9f84d8cc4671221562bbfc7d4f90e75713ba73d9b482d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.11.0-alpha1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.11.0-alpha1?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Mon, 04 Mar 2024 21:21:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 Mar 2024 21:21:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 Mar 2024 21:21:28 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd207cce71ce26ee9fc818f82a414e0356e86d4ff62ba8e35fc08937c3a0c76`  
		Last Modified: Tue, 05 Mar 2024 00:50:20 GMT  
		Size: 251.2 MB (251234011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4d6ac5a86916d83df669a9c711aef42cf82e4418e8a029ea588c1c4810dcea`  
		Last Modified: Tue, 05 Mar 2024 00:50:14 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-alpine` - unknown; unknown

```console
$ docker pull julia@sha256:9f4b7ddf4b2508e5f5f42e5387ca77e5fc0319f9867e4ea9d70a0fbe4dbcd30e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.7 KB (138718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae3ffb0e397f0444431222da65b14c5f48b179ed21b7da7de9ec5616ae0c219`

```dockerfile
```

-	Layers:
	-	`sha256:889462dc5a086a9eb40093d062e20b6a07cfe13719ba2f3fb860683af3e399ee`  
		Last Modified: Tue, 05 Mar 2024 00:50:14 GMT  
		Size: 124.5 KB (124491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f133203ac10cd0594e9818ab38b9a3bdc170def8a43ccfbfa325657a207f6be`  
		Last Modified: Tue, 05 Mar 2024 00:50:14 GMT  
		Size: 14.2 KB (14227 bytes)  
		MIME: application/vnd.in-toto+json
