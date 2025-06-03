## `clojure:temurin-8-tools-deps-1.12.1.1543-bullseye-slim`

```console
$ docker pull clojure@sha256:37f86320e73f4f7f71499b70981dccb5c67d8d53f3e5e9d7f427bc619232d686
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.1.1543-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7be4e289fd337d00a05055c5abb7c7b16876c559ac97d448e36833f97a93a55b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141715073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e157d07a499c0ac0a1f054c7f2e4addaa5ef50dcee6847cd7fa38c74ffac3aad`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:66850c8b65c1e9c3674a722b71f8887dd317a9b257148bb1063e88d85790544f`  
		Last Modified: Tue, 03 Jun 2025 13:30:45 GMT  
		Size: 28.7 MB (28746257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a26ea748e01f6fa271cb5c99f02841ad6f2c475c5d2be97781534dee920e77`  
		Last Modified: Tue, 03 Jun 2025 19:23:28 GMT  
		Size: 53.8 MB (53830497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffe5216b560673d57c7671a833a3544ee07cf7141d1265094071fc7b824d68a`  
		Last Modified: Tue, 03 Jun 2025 18:28:19 GMT  
		Size: 59.1 MB (59137676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0e98c10865614d54860a3f690566d02384379d2f9ad7d4e65984593a660818`  
		Last Modified: Tue, 03 Jun 2025 18:29:02 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.1.1543-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:da63afc3f7a9e93ce35ad03863d68b275e72d1b656643e353dfb175a96b1e259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5311035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1df0e076387a15d268ba4b23871cfc1d9e019232398da87783f32401e949fbe`

```dockerfile
```

-	Layers:
	-	`sha256:2ee92220cf1bb23acf2e788a9f3b05762e321af1f5bfcd898267d6ec9a7bdc0e`  
		Last Modified: Tue, 03 Jun 2025 18:37:19 GMT  
		Size: 5.3 MB (5296626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c8ff5dd15dd5470d77416dfa9e7aa00e56a6727a292daf14bb308e771f5cfc2`  
		Last Modified: Tue, 03 Jun 2025 18:37:20 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json
