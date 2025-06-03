## `clojure:tools-deps-1.12.1.1543`

```console
$ docker pull clojure@sha256:8ede2659206826a29acf6f32ba996f37181226fd945ce824acab42e800158770
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:tools-deps-1.12.1.1543` - linux; amd64

```console
$ docker pull clojure@sha256:cdd5d1c3ea11c73203115e4321ac092e26d5e58321d1d9bef149acf0b11b89c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 MB (287117947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f06a942fc5ab98e4edfbc558114fc3eaeed92c933dbb075b6771e1729023dbc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Tue, 03 Jun 2025 13:30:19 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa3c0578c3a59a8a3212a55463d1179d9abf668f220248eaea43297e31871e4`  
		Last Modified: Tue, 03 Jun 2025 18:41:31 GMT  
		Size: 157.6 MB (157634512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0d76532d27fbde4222b0a303a724a23739adc4146d84139dbf7755bb557431`  
		Last Modified: Tue, 03 Jun 2025 18:24:51 GMT  
		Size: 81.0 MB (80994153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d9a49e1e7e3cbdebb7be7e28b92bddf3f745a9d13914c35c5c57835cee7cbe6`  
		Last Modified: Tue, 03 Jun 2025 18:24:44 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760d3363eeb087e48beff429ae3cb911572b1d364e0d6beff8bb77dc31f3b743`  
		Last Modified: Tue, 03 Jun 2025 18:24:44 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.1.1543` - unknown; unknown

```console
$ docker pull clojure@sha256:9b346cefabccddd5cc21c6f0c648c29842dd61beb3a7158da1d83550fe0855b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7241445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5d77cf8ec38c90ebf7bc3d9398882e83f3d3f0436167cfeac38fac3e9f05595`

```dockerfile
```

-	Layers:
	-	`sha256:426c2c183ae1211a412eb590d65c84372d0b93bf3a8861753bf47350db86d9a1`  
		Last Modified: Tue, 03 Jun 2025 18:38:31 GMT  
		Size: 7.2 MB (7223624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea3d773cee9c0997302d854599a90a2d2663580f39ed135c505925e676bf9e0a`  
		Last Modified: Tue, 03 Jun 2025 18:38:32 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json
