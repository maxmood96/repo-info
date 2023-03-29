## `julia:1-alpine3.16`

```console
$ docker pull julia@sha256:ef54745a5c0cec59f68ceef82c726adefae2ccdcfd0746dfbf28de775ee25efe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:1-alpine3.16` - linux; amd64

```console
$ docker pull julia@sha256:f9d1c09e8b279f408f285b0ebd6206b508200c012799ba4279f7d961fcb6c3ef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137512177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad498e5a8daee1adfbf347d29cd896d7664a4126ba2e0aa3ce661e324f9bf10`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:28 GMT
ADD file:970e6b2578ef73457ffed1189e8ba128b0211cabd3174b8c7d3afd8fb58ad614 in / 
# Wed, 29 Mar 2023 18:19:28 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 22:05:09 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 29 Mar 2023 22:05:09 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Mar 2023 22:05:09 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 29 Mar 2023 22:05:52 GMT
ENV JULIA_VERSION=1.8.5
# Wed, 29 Mar 2023 22:06:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.8/julia-1.8.5-musl-x86_64.tar.gz'; 			sha256='12427c0336648b59f0c853b9885e2ffcd113e876d4b385b9cf59bc0e581987fc'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Wed, 29 Mar 2023 22:06:05 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Wed, 29 Mar 2023 22:06:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 22:06:05 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:91d30c5bc19582de1415b18f1ec5bcbf52a558b62cf6cc201c9669df9f748c22`  
		Last Modified: Wed, 29 Mar 2023 18:20:09 GMT  
		Size: 2.8 MB (2807803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5ef46b43d1ed595329d6acf6cc67b13066db2e009b71cb0252bb7b14ecadca`  
		Last Modified: Wed, 29 Mar 2023 22:09:27 GMT  
		Size: 134.7 MB (134704001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d50c2ff1d5842dff6db426d91a08049621752006ef46a946e7dc5e43ad129067`  
		Last Modified: Wed, 29 Mar 2023 22:09:06 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
