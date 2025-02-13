## `clojure:temurin-11-bullseye-slim`

```console
$ docker pull clojure@sha256:b62efd54577eccb2db6948b82959b7f8cd7a7a57acde132c7122c53982da756d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:bc7ac4c83c8672298afd089e9eadba5f259ab239ad17f7139e37359a1601071b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.6 MB (234639973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3c49ec6c5a992eed3efc1cd3611716cbb35b2f9fda53839bafce5cc33077add`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 29 Jan 2025 19:11:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 04:26:31 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c1ed3389592ebd62f037ed4217dbda6c5c503e15fe1229d040a3a0d9cb84ce`  
		Last Modified: Wed, 05 Feb 2025 18:16:28 GMT  
		Size: 145.6 MB (145598932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7a68aab7f5a04f545802d63736ccc8d758e4655709f04438da48dff98db3b8`  
		Last Modified: Wed, 05 Feb 2025 18:16:19 GMT  
		Size: 58.8 MB (58787810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e362232ac762ca552a2c550f67f74596f921d429a55084253da1c57b120e19bd`  
		Last Modified: Fri, 07 Feb 2025 08:55:37 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:950f5edde22d2055d747283a34658d338ed4e5b9b2f22bb7d8313d87b2a1846e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5151518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cede56ddcddb000a96f515dfb7b925a2b1254a15651ad5daa62811a69fa8c20`

```dockerfile
```

-	Layers:
	-	`sha256:b1f45ecdbdc1754d3b6bcd5f1f3724988d001a04c5a6ad28663ceb7a0863b760`  
		Last Modified: Tue, 04 Feb 2025 05:21:04 GMT  
		Size: 5.1 MB (5137208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:077b15c7b9b137d0eb7b1e8b3c82749b6f40bb9f4a8e3c33e9f0c0f98a37b5b0`  
		Last Modified: Tue, 04 Feb 2025 05:21:04 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:92a60cd23e50f375db5b9ac95881de2a5720ab0b82a9743934f49bc5f9322aa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.0 MB (230039902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c9c8acb6601628864e958c419e477769bdc9fdb06b85a3b868dc8b2fc16655`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 29 Jan 2025 19:11:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9225a2a808e874449ee822a282882a3c331aad2f5093c1062e16494d8bce3e9a`  
		Last Modified: Tue, 04 Feb 2025 04:27:50 GMT  
		Size: 28.7 MB (28744810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8d675225baaf53e26e9c42dcbe4bf812ba2ecef1c2c7500ee0fa37ceace522`  
		Last Modified: Wed, 05 Feb 2025 05:45:54 GMT  
		Size: 142.4 MB (142385434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f724a94386608d16c7441cdd1ee76a3b7631f670dbce2c83628050d3f6c71e7`  
		Last Modified: Fri, 07 Feb 2025 08:56:22 GMT  
		Size: 58.9 MB (58909014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edef41224a06ab0144feeeb6c1e91a3a3abb753c3f5d646c725c2eb431a39f07`  
		Last Modified: Fri, 07 Feb 2025 09:27:54 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:83657f0a80b260fddea12f083af3265e83ac5ab5f95082466c229bcd740155dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5157986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c5a20a798ec14b657e338a18cd2f3849efc0a5fda2255953cb9e0d5f02514f`

```dockerfile
```

-	Layers:
	-	`sha256:9b48af1191446b1a650cc044673d5ddb979b318f349c662db86e7fa59e036848`  
		Last Modified: Tue, 04 Feb 2025 23:40:29 GMT  
		Size: 5.1 MB (5143558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1571f748c960d26f7637526c5f681044af6f05efeb4c736d9ea6959c7cfa3869`  
		Last Modified: Tue, 04 Feb 2025 23:40:28 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json
