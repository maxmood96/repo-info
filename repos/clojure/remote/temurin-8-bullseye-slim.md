## `clojure:temurin-8-bullseye-slim`

```console
$ docker pull clojure@sha256:88ee33dfd961c247222958fe1653d888d90fcc6f38a95b2672e59c4725a8d980
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:cd98f71bf95f13977bacc609bfd13fb1be8983c6d47ee9a7627202ecfaa6cf34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (143978495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eda09ced4520886d2f40c2d2983e6241a8f0e3aa99caaf50dce2f8c97a132d5`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f43fd7ebcbac771e65e7bd272b57da94f5c997c73dd02e3fdc7a6351b1da8ff`  
		Last Modified: Wed, 04 Jun 2025 11:30:36 GMT  
		Size: 54.7 MB (54716181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031c8bfa9bef8c03a19a3530e53cb86b43b0476b27719d813dc6b4ef9d7c62d3`  
		Last Modified: Wed, 04 Jun 2025 11:31:00 GMT  
		Size: 59.0 MB (59005729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6eb7ff3f28fbbf4b1a4a0e6ef2fbc328af8dfbc65c30bb66a9a992ed0a47a9`  
		Last Modified: Wed, 04 Jun 2025 09:23:07 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a505255132a3e4dcaeedf9361447ca8110412070afe234e6c2a604819a21a7d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5304487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e506ff7ce4a03d1cf7517bf3a71e42395c75748da369b854052c9968e046d1`

```dockerfile
```

-	Layers:
	-	`sha256:15609903d971655b6ae6b24acff0014fcc299f6f3f3bb89cc06a5fab1db53046`  
		Last Modified: Tue, 03 Jun 2025 21:44:22 GMT  
		Size: 5.3 MB (5290196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f32273f4e6e75bd3761daa85d6e03004785c39a8ce569f603ec70a8d70f7fe0d`  
		Last Modified: Tue, 03 Jun 2025 21:44:23 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye-slim` - linux; arm64 variant v8

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

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

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
