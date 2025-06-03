## `clojure:tools-deps-1.12.1.1543-trixie-slim`

```console
$ docker pull clojure@sha256:682f6ff72f9898085ff32ccc35b1af631d599d053a37747be40f2f769f90ca82
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:tools-deps-1.12.1.1543-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b175d41bc344108151e6600dc9ed5d109ab5d4a7893805a33df1e0eb2ae42c26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.1 MB (262056321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa42b6417dd1ba70009fad80b6fd3b75babccc7beee246d931956c5a444dd3c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
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
	-	`sha256:ced038dea045df288fe9bdbe03117ca66fe2a071217e196ac86ed07f965fe688`  
		Last Modified: Tue, 03 Jun 2025 13:30:48 GMT  
		Size: 29.8 MB (29755384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d381b01eb8a80d0a69cb9011ba33dcb59c98ed8503af0ab673a07c1df65c0fae`  
		Last Modified: Tue, 03 Jun 2025 18:24:27 GMT  
		Size: 157.6 MB (157634512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d26d8c69150e8fc803f3b9e060db8bd84d8ec57f553a19d059407329c483f371`  
		Last Modified: Tue, 03 Jun 2025 18:25:06 GMT  
		Size: 74.7 MB (74665382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0959d92050d685b48443d6d0899f27091edaaabfa98210c40953ab49654c264b`  
		Last Modified: Tue, 03 Jun 2025 18:25:02 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd39c2ea3e53e926ce4e55b52c9deb3bacba822b93744e80e070a5c97d4d795`  
		Last Modified: Tue, 03 Jun 2025 18:25:02 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.1.1543-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1d77dd29f854c4973072de8d4175cedbc2f36af44883ba2c729af7a131f84977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d912de538cad3eeb975a632128b941643406aec23ed27c2122e4e21a0da5e27`

```dockerfile
```

-	Layers:
	-	`sha256:b0052a07ff48db55ff52d41ca3a85be1e3b9fa7e2ccdb7ae206b8a622c66cc87`  
		Last Modified: Tue, 03 Jun 2025 18:38:47 GMT  
		Size: 5.1 MB (5115855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:457c6e0236610f3938d5d0f1913da93d8d402faee5a1b4e58f6bb68a80953b00`  
		Last Modified: Tue, 03 Jun 2025 18:38:48 GMT  
		Size: 16.5 KB (16543 bytes)  
		MIME: application/vnd.in-toto+json
