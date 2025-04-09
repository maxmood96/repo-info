## `clojure:temurin-8-bookworm`

```console
$ docker pull clojure@sha256:7220648534815e912b812810d31567ebc880ab8f1fa4de5d51a05a20dd290471
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:a94317de7942bef494a2ce5403b3f2a681f2384f3c8313a149be25dd7fee1796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.2 MB (184206163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ddf047a50c5a50ee367813f13fabf43ed75ae659dd0776819f91d96e90a7fc3`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:23b7d26ef1d294256da0d70ce374277b9aab5ca683015073316005cb63d33849`  
		Last Modified: Tue, 08 Apr 2025 00:22:55 GMT  
		Size: 48.5 MB (48490541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263cd050ec5c581f103821a6e72683b3533adb8bfae343280063241277e689dc`  
		Last Modified: Wed, 09 Apr 2025 02:18:07 GMT  
		Size: 54.7 MB (54721244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9634936b7e59f532f8977d9ee4ea5db387bf6a85b4b66d7df04b6b01aaff91b`  
		Last Modified: Wed, 09 Apr 2025 02:18:07 GMT  
		Size: 81.0 MB (80993731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98760b0422927f5716f9c88def46aeec0d78a6bc8162ba6ee4f0ade4bc7e063`  
		Last Modified: Wed, 09 Apr 2025 02:18:06 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:183a9dc28bd2d0dbf759d5782da58996b8e773538de4ff16513ba8b34f4cf620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7308323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d6e98d1d11e8ebf7fd05822426ffe9aeb7f98a2e86ff07bab1cf15d2dc09fa3`

```dockerfile
```

-	Layers:
	-	`sha256:c5f7ed47de38640745597033fa50d4183d81ec95eac3581bdb0ba0b0c405e807`  
		Last Modified: Wed, 09 Apr 2025 02:18:06 GMT  
		Size: 7.3 MB (7294086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41143ff55ae169a23b183217bdc7d48897b4ad3cd567a37e157f90457b55d677`  
		Last Modified: Wed, 09 Apr 2025 02:18:06 GMT  
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
