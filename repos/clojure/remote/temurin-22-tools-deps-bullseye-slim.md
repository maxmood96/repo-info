## `clojure:temurin-22-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:388e9456876269514f50b0360d56c20c8b3c4e4a63da733000fa0dd04bf58b84
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:8fb3f4b4cf5f8aaf26973000f067c30b38051ca0bcff861f06d9c7d5b39b15f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.6 MB (246570929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83b68bd0b801d139920490a9aec336903140aa2f61d28171a4d77e42ed448790`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a930731f74f240cd4db43f3c95b479d152eb955c5114bba32edd3a6a683aad`  
		Last Modified: Thu, 13 Jun 2024 18:14:14 GMT  
		Size: 156.7 MB (156715500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8707816b27b2ff83ba51ad63e4bb9545a7fb28bc5751a962f3e7465d1957b2f3`  
		Last Modified: Thu, 13 Jun 2024 18:14:12 GMT  
		Size: 58.4 MB (58420343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61cd525cbd8f33061c336b1b1e71ea9abbb4efe10b51e85ecc1aad9b6903d33`  
		Last Modified: Thu, 13 Jun 2024 18:14:12 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928b699b83d55748b9306c7fcfa666d7d189f5cbfd6a286dd6a0eaa588433798`  
		Last Modified: Thu, 13 Jun 2024 18:14:12 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4bc6a0d663b90a352b86c1bf9efe0d1b7eb674e0d14ee4b59b1b3fe8985149f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4924739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5477d76e0759afef5db44bc37a4aad7aadf3a5f8d7c4c601465e8ebb1508b8d8`

```dockerfile
```

-	Layers:
	-	`sha256:1230ad01ca366c239d35c791bfc7053c9d4827ddf1de4e69e9bb68d4e7d46081`  
		Last Modified: Thu, 13 Jun 2024 18:14:12 GMT  
		Size: 4.9 MB (4909227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7c06c07dac96f419f9ffc9083dee745d4323f9791f101628c8d7729719daed7`  
		Last Modified: Thu, 13 Jun 2024 18:14:11 GMT  
		Size: 15.5 KB (15512 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:acd1c7c9645103be0e19f1a4e250df8d6905b0a0e2b7fdfa4d017ee5e42f748e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.4 MB (243366144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5320829304cf3263e2d4d009e9a343fde366432e9e11331947eac6b56b7f9082`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e350b39c02b326f486ab2d8c055400ccba7ecc5d7dec7063c51b58e95ad06226`  
		Last Modified: Thu, 13 Jun 2024 12:02:23 GMT  
		Size: 154.7 MB (154738000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8fb91ce70e9339a3e64a29e743242388596c23c26399bb387b996f2d7b1782`  
		Last Modified: Thu, 13 Jun 2024 12:05:36 GMT  
		Size: 58.5 MB (58540125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cffdf07b10170981ce9d031b056a7c3be344d8261b5ebfa2d92a4593d864e70`  
		Last Modified: Thu, 13 Jun 2024 12:05:34 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477638b089c25d68ca76ff6e9749eeee41b0d5f8750e4919141ac748c8146584`  
		Last Modified: Thu, 13 Jun 2024 12:05:34 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e64be63612d7090bfc96ea8a0bad89294745822064e55c94c6eb559c42f702c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4931635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0374d2a7f282fd48cfa1d00ce6f55fea5d786cc07b3b85c7692b73b0d3ff0593`

```dockerfile
```

-	Layers:
	-	`sha256:b82f30be7cd70f1a2be7aa932537cd31f095f238e9de7ab37f43e21a141c1aec`  
		Last Modified: Thu, 13 Jun 2024 12:05:34 GMT  
		Size: 4.9 MB (4915583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ae9187b7c0663f3a52ffb526077b4cc1b538f5e9b3df973864e82ae86a1ec57`  
		Last Modified: Thu, 13 Jun 2024 12:05:33 GMT  
		Size: 16.1 KB (16052 bytes)  
		MIME: application/vnd.in-toto+json
