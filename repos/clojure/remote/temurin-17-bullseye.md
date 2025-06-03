## `clojure:temurin-17-bullseye`

```console
$ docker pull clojure@sha256:61de4fbb5da13b610e0cb36564f202f238dd9846660bb02b8423357e64cdbeec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:0ad1781c651b5f270e656bf281105e83a1e9e1ffde107432cfb4aaca743d58b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.8 MB (267796378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7d1d73a6e37688dcef66ac8dbd2807796d74e6bbce1cdb550e3d9eef80bd363`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:54107f2de180b7b6e9f909d2f1c6c18e10c700a6bd80a035d931768b06bb2905`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b737acf4b958ac359a27600403010080be11f872fe5f733f5ee66f363a32b67`  
		Last Modified: Tue, 03 Jun 2025 18:24:09 GMT  
		Size: 144.6 MB (144634963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f011b04975ef5f37c8bfc496f984c9912c6d8924d4734b8ae80a7e72ed74709`  
		Last Modified: Tue, 03 Jun 2025 18:24:57 GMT  
		Size: 69.4 MB (69410182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e1a0802d024a2e3af032bb81b949d6b0eed26c973264837b5785913ca9a14e7`  
		Last Modified: Tue, 03 Jun 2025 18:24:43 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e961bec175e57db611deb45b929c27486fca8cc300b3999cf62aa58fd8f91a`  
		Last Modified: Tue, 03 Jun 2025 18:24:43 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:cced41f8672704cde693c983a901300c5adf22a75b397a05550503a33ecfbf2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7272007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0a4478cb5e145f4f4cc7292a0abbfe67d9c9c442c8d9dbb8a85992746bc04cc`

```dockerfile
```

-	Layers:
	-	`sha256:d916d7a3d582f864524537b8721b905c07e4223ae3249694ec592dd843d5a7e0`  
		Last Modified: Tue, 03 Jun 2025 21:37:34 GMT  
		Size: 7.3 MB (7256186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a6ac9d6d4eb1335a6cadf043a1daa8439e62d13f8bc92055ced1549eb276ff9`  
		Last Modified: Tue, 03 Jun 2025 21:37:34 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:96baf18850232f896818d3f24f5e8b197f8df17f4f9efad6b26c305457b73f31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.3 MB (265299433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad173b82a69dbddd36e2e72396726f28702b7b536426e95cc9c6b280b2540291`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b2737025fe8da5b868f566cb4e3dc3330028cee06c83db854f56467eca6e09b8`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 52.2 MB (52247755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade6077201c8ba74fe01e7c07b8390be588631d5529c12c56af96a10c977df0e`  
		Last Modified: Tue, 03 Jun 2025 18:40:36 GMT  
		Size: 143.5 MB (143512642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b701242fc5cd71dbcae26902fbcb40da2a2d097dde8599bab38e5297795c8509`  
		Last Modified: Tue, 03 Jun 2025 18:40:42 GMT  
		Size: 69.5 MB (69537996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0dea675e287146d8e5c2ce7926f0d490c982de9aec7b315f88bb8a0ac4d8f1d`  
		Last Modified: Tue, 03 Jun 2025 18:40:26 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a236819df4139d8d6cdb0279f256260abc488dbf546e9d7fde20d7876a7fe011`  
		Last Modified: Tue, 03 Jun 2025 18:40:26 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:e5b1b1fdc9da27ba81d03bfc4fc339642a158e609f9fdc8aacb7bcf181714c68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7277224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f396b2efb006a1a35505ae6e1cfaf7fbacf6b4d2162cdd23abff537ea7967b5`

```dockerfile
```

-	Layers:
	-	`sha256:d7a1e0fa76991865190fe3bdd0f9e40acab8a2aab2df63836c87df29bd21d72d`  
		Last Modified: Tue, 03 Jun 2025 21:37:40 GMT  
		Size: 7.3 MB (7261285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6e5a04eb909bdec0c26ad68499b9e7ad6dcd3d41d514240a7e6e41ddf085348`  
		Last Modified: Tue, 03 Jun 2025 21:37:41 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
