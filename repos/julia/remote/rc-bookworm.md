## `julia:rc-bookworm`

```console
$ docker pull julia@sha256:790c4c69c810721f4891cae96d30e8724eb9149a8eda51d0170b5be662da4af2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:rc-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:4b1a903c980f511da26a8c3853e5bf9dfeb366b98a00cb2d04e514dae23b637d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.1 MB (329060458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:812efcb9dd0473d9eb5327afb50cedd599e1331979895089bedb056c050d10b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 05 Jun 2025 17:59:29 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Thu, 05 Jun 2025 17:59:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 17:59:29 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 05 Jun 2025 17:59:29 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Jun 2025 17:59:29 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 05 Jun 2025 17:59:29 GMT
ENV JULIA_VERSION=1.12.0-beta4
# Thu, 05 Jun 2025 17:59:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-beta4-linux-x86_64.tar.gz'; 			sha256='cead6a6ff3464af359258579a3ff6fb1d6f65aa93cb7b32b00691c23752f1cd7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-beta4-linux-aarch64.tar.gz'; 			sha256='e8ae058e3534a979de94688786f546060bbc676ac06035cd4350fbc53a1ddc21'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-beta4-linux-i686.tar.gz'; 			sha256='748eabeb5a31b9eb096b641010d1a0a9bf63283f58425734660c1056ba790e55'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 05 Jun 2025 17:59:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:59:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jun 2025 17:59:29 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db367afc96b68ce5d38fdf196e0a3cc1055592ed0b5d0534bb8ae3aafedb399`  
		Last Modified: Tue, 10 Jun 2025 23:29:14 GMT  
		Size: 5.7 MB (5714638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf28127661bc8e000b0ccddfb7966ef587587eb9f7362b181b5564a366bca838`  
		Last Modified: Tue, 10 Jun 2025 23:28:50 GMT  
		Size: 295.1 MB (295115318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c178c42687a6560e6857ed4c64306f4ab8b7988be0ff6c31c126472c48af9d`  
		Last Modified: Tue, 10 Jun 2025 23:29:13 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:0f949cc507ae997d1abe45c2b7ceddf4b750b61f0851be9cdc4be63952559772
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2582100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d8fdf69ba48d78a160becf0fa5a08b2dbd3a487ca359078542463b47ebb9e76`

```dockerfile
```

-	Layers:
	-	`sha256:27d2d284a6295cfec49adfc47a478fc52d3aee863d9f1478a38a9a51001e7a02`  
		Last Modified: Wed, 11 Jun 2025 02:03:39 GMT  
		Size: 2.6 MB (2564829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9580e4e4f1d7cb6ee1fd541e38b0741a53cb351de42ab7eac15121a2d14b8b9`  
		Last Modified: Wed, 11 Jun 2025 02:03:40 GMT  
		Size: 17.3 KB (17271 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:bec2ea9fb5a80204d08e2d53354ddf2330f91b4ba3e5c4c12e6d2670bacee2ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.5 MB (350453168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d71b6c85eb06800fccb915c5a3b036047334c61a6946e85c7b84fc5e117c0348`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 05 Jun 2025 17:59:29 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Thu, 05 Jun 2025 17:59:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 17:59:29 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 05 Jun 2025 17:59:29 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Jun 2025 17:59:29 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 05 Jun 2025 17:59:29 GMT
ENV JULIA_VERSION=1.12.0-beta4
# Thu, 05 Jun 2025 17:59:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-beta4-linux-x86_64.tar.gz'; 			sha256='cead6a6ff3464af359258579a3ff6fb1d6f65aa93cb7b32b00691c23752f1cd7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-beta4-linux-aarch64.tar.gz'; 			sha256='e8ae058e3534a979de94688786f546060bbc676ac06035cd4350fbc53a1ddc21'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-beta4-linux-i686.tar.gz'; 			sha256='748eabeb5a31b9eb096b641010d1a0a9bf63283f58425734660c1056ba790e55'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 05 Jun 2025 17:59:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:59:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jun 2025 17:59:29 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494d7707679467d6f74949463d626bb5429903a4f930fc3d1287e16489f516fa`  
		Last Modified: Wed, 11 Jun 2025 00:11:28 GMT  
		Size: 5.5 MB (5541558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0331bdf10e365abffc334873c2ced93ebd47b666a12708cdb834604b5ff0e59`  
		Last Modified: Wed, 11 Jun 2025 00:11:37 GMT  
		Size: 316.8 MB (316833561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df2a0295f13c11a3e39721501105a5866050fc2221f800dc4da9ba21ea202d0`  
		Last Modified: Wed, 11 Jun 2025 00:22:44 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:b99a15a4fe11c8dd1c660630d32cf5193b9ae628e924fecdfc920ee6add590f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2582542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e2ec2b4d1217b0c69abe45c0a8e9f6c1000667f4d6c3dbec686c396f8e222f7`

```dockerfile
```

-	Layers:
	-	`sha256:3f0fe155d890988450bd249d65c402114032f46d09fb1be734c8d55fe662a14a`  
		Last Modified: Wed, 11 Jun 2025 02:03:45 GMT  
		Size: 2.6 MB (2565128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:694a71b962781d49d0a6be9183340d57d42eb1270645fdf3e2ad57d27e92ad7e`  
		Last Modified: Wed, 11 Jun 2025 02:03:45 GMT  
		Size: 17.4 KB (17414 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bookworm` - linux; 386

```console
$ docker pull julia@sha256:a711358b24c4116e02f055b5417a4cc3e43db1c42e18bd26503bd01ca10b4563
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.3 MB (272298495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a27c9b9a0963309bd5cfc1b22dd04df31e991d95edfb6bc03fd98288d06c9cf3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 05 Jun 2025 17:59:29 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
# Thu, 05 Jun 2025 17:59:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 17:59:29 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 05 Jun 2025 17:59:29 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Jun 2025 17:59:29 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 05 Jun 2025 17:59:29 GMT
ENV JULIA_VERSION=1.12.0-beta4
# Thu, 05 Jun 2025 17:59:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-beta4-linux-x86_64.tar.gz'; 			sha256='cead6a6ff3464af359258579a3ff6fb1d6f65aa93cb7b32b00691c23752f1cd7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-beta4-linux-aarch64.tar.gz'; 			sha256='e8ae058e3534a979de94688786f546060bbc676ac06035cd4350fbc53a1ddc21'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-beta4-linux-i686.tar.gz'; 			sha256='748eabeb5a31b9eb096b641010d1a0a9bf63283f58425734660c1056ba790e55'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 05 Jun 2025 17:59:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:59:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jun 2025 17:59:29 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c3d46fed134488b3ee18c12cb308c8d5520b8c647122c392f9fb76e3e1e2fc61`  
		Last Modified: Tue, 10 Jun 2025 22:47:25 GMT  
		Size: 29.2 MB (29212433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6afdfb9e1d26d40ed7e85217f4b60c9cb6d26d99cf597d24f4b1cd26c7da5892`  
		Last Modified: Tue, 10 Jun 2025 23:28:29 GMT  
		Size: 5.9 MB (5874785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f346267c5629886528340cfd8c326d180bb277aad32c83effe8afef3aae39d`  
		Last Modified: Tue, 10 Jun 2025 23:28:04 GMT  
		Size: 237.2 MB (237210905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c417c8d0a875c682d57eb7fae5a85ea637d317a4b96f0152de4d881838c9d0`  
		Last Modified: Tue, 10 Jun 2025 23:28:29 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:fd93df343fee2f049702c003f05c2af50ce1bb0407ac84c0361dfd8dfc0341f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2579193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66255ee59fc494020e6702f7caf8329b474bd8334e3c2ccc2a3b85fd24b6cdc7`

```dockerfile
```

-	Layers:
	-	`sha256:f74241f96f04f58bbdc2288b9c724301e4b5805ed0b53c1fd7fbaf27bfa50e3c`  
		Last Modified: Wed, 11 Jun 2025 02:03:50 GMT  
		Size: 2.6 MB (2561966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b873417a85c9cefc7311a84d5f1687990aa10a97d485556ba477b16330b785ae`  
		Last Modified: Wed, 11 Jun 2025 02:03:52 GMT  
		Size: 17.2 KB (17227 bytes)  
		MIME: application/vnd.in-toto+json
