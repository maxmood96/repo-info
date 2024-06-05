## `clojure:temurin-11-bookworm`

```console
$ docker pull clojure@sha256:e46f966e83039ac4a31b9e5c89b52915b05558b7da85d2741912204131edc538
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:d8ffe171823d05ac7e2ad002db542c7d7cd1b62586eefad6969d5a547ed8ceac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275381691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf61ef1646a4b5a244ab7c14ddd25ea22c9745c0e3283d1426d9da6dd8f58e31`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 14 May 2024 01:27:51 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 14 May 2024 01:27:51 GMT
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1806f741e5fa838a221acff1b5807a0c4cddbb935a8b812e19ad87a0e553ea7a`  
		Last Modified: Wed, 05 Jun 2024 06:10:21 GMT  
		Size: 145.5 MB (145505214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6f45be0a4723943683a32b1f74c9956ae77a6d6ad50c9375a1f0cbc8474e501`  
		Last Modified: Wed, 05 Jun 2024 06:10:20 GMT  
		Size: 80.3 MB (80299440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc27fbaf49f75245bd805ce5b402387ad594f86edbccced91b4164f3bfcd377f`  
		Last Modified: Wed, 05 Jun 2024 06:10:18 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:264585a204c8907daf3ce290eeb7da2942b493d42592897c5124a8f27f981265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6974481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12fb594d524c6a835030ace6613d6c6329dab3b0d96b5798db0e58fe8a518d63`

```dockerfile
```

-	Layers:
	-	`sha256:4afc5383fd7cf50eadbbe0de625cc217abf0d0455d61453e12b4347bb1eb3628`  
		Last Modified: Wed, 05 Jun 2024 06:10:19 GMT  
		Size: 7.0 MB (6960666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a816f3a2cbf6d19e863307e8b9af45ba841e38d96390b5fe9b5f2114aae0ce0b`  
		Last Modified: Wed, 05 Jun 2024 06:10:18 GMT  
		Size: 13.8 KB (13815 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:58320358ea721f4d63d3db60620d961939b7f93ea69c4d5f5cba313dd7462426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.0 MB (271963345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e3525e7860c7121c874e698835f0a3edcc5fdb8e64770d0c19b8e8df0e749af`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 14 May 2024 00:39:32 GMT
ADD file:b7c55dda8ded4219a7cdc9fbd91dfb5996c4886d4394b85751c2f956defe3287 in / 
# Tue, 14 May 2024 00:39:33 GMT
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:91e301773f03e9e0fabc5c177fe6bfe8daf14e992ab816f151692b814ddc462c`  
		Last Modified: Tue, 14 May 2024 00:42:35 GMT  
		Size: 49.6 MB (49613388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad0a59b38387ea00b0bec1334650d2cb14ac6bdfe36c559e2a4c6670cd73a955`  
		Last Modified: Wed, 05 Jun 2024 13:41:49 GMT  
		Size: 142.3 MB (142304039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4970db0749271dd54e9e5e15a87b953aa7683fc547a05fa3435353ea3e5cbf21`  
		Last Modified: Wed, 05 Jun 2024 13:57:59 GMT  
		Size: 80.0 MB (80045270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8449b3285d909f6ed0633fe52b4c4e8c3272620b8c8eea7f31f79ecb9475e0a4`  
		Last Modified: Wed, 05 Jun 2024 13:57:57 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:8e59050c0a3a976469433644dd29e916b43dbc6d779726747d5ddb9787ddc240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6981404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deab731f61c31218c7fdc649261e5efdc06548bbd004f60dfe7acf1acb16aed2`

```dockerfile
```

-	Layers:
	-	`sha256:20f1045f9f2071c786953b5573453236253e1a7d30875bea0d60b7292a1cfb32`  
		Last Modified: Wed, 05 Jun 2024 13:57:58 GMT  
		Size: 7.0 MB (6967053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a3bfa72fb4d5efcba03b9fc2d127c98635256380d82af3abbb70bd85354c453`  
		Last Modified: Wed, 05 Jun 2024 13:57:57 GMT  
		Size: 14.4 KB (14351 bytes)  
		MIME: application/vnd.in-toto+json
