## `clojure:temurin-21-tools-deps-1.11.3.1456-bullseye-slim`

```console
$ docker pull clojure@sha256:9b585834afeb55194f30122f1f95be89cfd17f1bf20a59d013200e34986b58b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.11.3.1456-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:714d840a1449023f58263847852af94f7f27f1fbf43b181139fff9c8dfec2d7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.4 MB (248352308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dc3f10dc10175ecfcee46a6e0633b2b58a24d002e6b83f6fc526fd0f3241c74`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7080db256fffd5c8d1202dac128df392b0494c474ac393236cdc1e6595da464`  
		Last Modified: Wed, 05 Jun 2024 06:12:30 GMT  
		Size: 158.5 MB (158497956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae729e2fd3d134d8c8f96e4578a3aee654eba4bb97d0d7ee8dd9838786ade610`  
		Last Modified: Wed, 05 Jun 2024 06:12:28 GMT  
		Size: 58.4 MB (58419377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ad38075136b5030c03e50c39558a6a4d87587dcf34f8846e8783758740965c`  
		Last Modified: Wed, 05 Jun 2024 06:12:27 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae955c8c4e15230535624fafed0937198a3d9c653f5e7f2f2c59fc0c84da8e9`  
		Last Modified: Wed, 05 Jun 2024 06:12:27 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.11.3.1456-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:49744985092ec2acb952fe0fb8b36be1cd727a540c6bd517f16d4dea6f007fcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4926098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55236ef1937ba432b84025ccc8fd0be97f4a470f63254ba8c75b21e84299d77a`

```dockerfile
```

-	Layers:
	-	`sha256:9f4bfa93ae59696a82f9330f2c9cc7f982ebd335c6758de76b561b73ffb36039`  
		Last Modified: Wed, 05 Jun 2024 06:12:28 GMT  
		Size: 4.9 MB (4909939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42ffdb852a1ae65e8efc8efeac64070ec1bc84ad6d49371c057affd841c90027`  
		Last Modified: Wed, 05 Jun 2024 06:12:27 GMT  
		Size: 16.2 KB (16159 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.11.3.1456-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:476af18ec09dde10cce2c8bdf1d90306b1b922e3097ad10b8e14eb767af4211f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.3 MB (245293715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:489d45e8b12e0effffedff9ba5b1f155fc0dfee5681e02bc2d7061fb0156fc17`
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
	-	`sha256:b564c25575a74b32dc66c660031ab1490f376022bf7649dbc787565d8d624ecc`  
		Last Modified: Thu, 13 Jun 2024 11:55:25 GMT  
		Size: 156.7 MB (156665603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c4395531b57b9297e6482780146a12ee3e43b0756801083f18dc44dde387bf7`  
		Last Modified: Thu, 13 Jun 2024 11:58:39 GMT  
		Size: 58.5 MB (58540090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7df60427849291e07912f0b4d52e0c6ab918ccbec5920db164d777663f03714`  
		Last Modified: Thu, 13 Jun 2024 11:58:37 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9142cd0cd47e66744a097f3cbfffe000be70f82efc865d9ee44042de74174ba0`  
		Last Modified: Thu, 13 Jun 2024 11:58:37 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.11.3.1456-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4380d255625e1c9e7abaee2689d4eaa69745cabc3bee02f57e58c967bb8ef84e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4933092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9049262c6963c2e659c1ac5c0d91f91c8885648224353083bef943e29c22c73a`

```dockerfile
```

-	Layers:
	-	`sha256:ef2a1283ab590db748cafd4e6b22ce30bd29ddf3cec6ca18ccad7568e6219867`  
		Last Modified: Thu, 13 Jun 2024 11:58:38 GMT  
		Size: 4.9 MB (4916319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30c01cfff1e4abd4c093be53a99c139bd5130c0fff82c969eae73c11304cfb55`  
		Last Modified: Thu, 13 Jun 2024 11:58:37 GMT  
		Size: 16.8 KB (16773 bytes)  
		MIME: application/vnd.in-toto+json
