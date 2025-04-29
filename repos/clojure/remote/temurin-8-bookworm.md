## `clojure:temurin-8-bookworm`

```console
$ docker pull clojure@sha256:f9fa2469c1f3557987d657ca731536acd1de761a28c1e81e6515ea42f4ec05c8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:705188b78e5f0886cb2621a0db84b0d26a303cddf9803da182c3dfc7aae06291
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.2 MB (184199363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ed5717f31cae26cb8ffcf0a8621ea2b8c9c869ae5c61c703f599c641974fe86`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ae857c483d9db15f355917316c91aceae5e787cac978212c74ba565a9dc1cc`  
		Last Modified: Mon, 28 Apr 2025 22:05:51 GMT  
		Size: 54.7 MB (54716178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22900c958937a4682aa023a26aea6aaf034cd60b87244a3cbd7d9d4592711fc2`  
		Last Modified: Mon, 28 Apr 2025 22:05:54 GMT  
		Size: 81.0 MB (80991342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290a85fcb4408343e9dcf0fc793035b7d4994ef55681fc97426c4b9445b39780`  
		Last Modified: Mon, 28 Apr 2025 22:05:51 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:61f0474d9eb17d06e8fc1f0d79f79d6de5c93e81c486075b624086301274d49a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7308323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da85ba03be32293fadc7349a50288ddfa02c7e3cd9d26839d951cb9ea288f2e4`

```dockerfile
```

-	Layers:
	-	`sha256:fc8822df51fb782e7546c67bd48cd53098c96e35619f8dccf558a69470639eee`  
		Last Modified: Mon, 28 Apr 2025 22:05:53 GMT  
		Size: 7.3 MB (7294086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9496d7e494ac1e2c2e7267ee6c941bf57300a990f7d9e1754fea4be226ef9ce8`  
		Last Modified: Mon, 28 Apr 2025 22:05:53 GMT  
		Size: 14.2 KB (14237 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:da94bdac0106af95e659bfd2188e0ca0f735fd14c75d8951f2b77b1c30a318e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.0 MB (182993558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898b315d58eef13d529a0120ae7820699a4dd78a272fa412596481ca818355ae`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:71daa2c787b0984bbf3b93b60686fc9fe305d28e833914019b2745ab9f36730e`  
		Last Modified: Tue, 08 Apr 2025 00:22:46 GMT  
		Size: 48.3 MB (48327469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ade19d999a343e293e6efaf9289e399b21e9b8ce40c7cf413da3be24bd068c`  
		Last Modified: Wed, 09 Apr 2025 17:11:37 GMT  
		Size: 53.8 MB (53822768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24e60275c75f38faf287b241bcf4045f5423cde561126b1488af2329debb00a`  
		Last Modified: Wed, 09 Apr 2025 17:16:23 GMT  
		Size: 80.8 MB (80842675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36221fc2931b128e4f912f532fb5864b8765cbeefcaa6ffd3ea6a7aa08f320b0`  
		Last Modified: Wed, 09 Apr 2025 17:16:20 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:9bed7b787c569904630fe4f957ae5c4e985b27bdea472e81e790a0bb3bd33e17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7314902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32f3f7610c373b41c91bd45b9f701e82512f5bb27ba9550453f4606adae053ce`

```dockerfile
```

-	Layers:
	-	`sha256:ec58befe85e7a501ab8588ee105e127fe39e7c0d58d92d5b485856549a3ea06b`  
		Last Modified: Wed, 09 Apr 2025 17:16:20 GMT  
		Size: 7.3 MB (7300547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71e74f1c9fb5d8f63b9df29adb0a0e9c9fc001196531bb74248f3aef4737ce89`  
		Last Modified: Wed, 09 Apr 2025 17:16:19 GMT  
		Size: 14.4 KB (14355 bytes)  
		MIME: application/vnd.in-toto+json
