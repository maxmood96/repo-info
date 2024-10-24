## `clojure:temurin-23-tools-deps-1.12.0.1479-bullseye-slim`

```console
$ docker pull clojure@sha256:5546ee0db7673439650d6994db31328b9a79c58c890aaed513c3a4483817004e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-1.12.0.1479-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c6caef7fc7ba5155b364d0b9b754ab84ee2ac47a78e0f0d71ba1aaaf66e91b0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.9 MB (257937185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46449b0e9fab9d3038fe2dbe8e9de8df1e3c0e4f7b9c5dda28bc74adfcf358d5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31b00529f6a07fa13203c73dbb73bf57711d15e799134c92f5b39527478ecc3`  
		Last Modified: Thu, 24 Oct 2024 01:57:02 GMT  
		Size: 165.3 MB (165295127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9ad66f085b36daff02a2bf07175c119ab48a1b352c19517d12eacb56aa48d5`  
		Last Modified: Thu, 24 Oct 2024 01:57:00 GMT  
		Size: 61.2 MB (61212215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d69737b5b608f7b94fc0a9615fbc844fb81b6357ea27337fcb74be951de1859`  
		Last Modified: Thu, 24 Oct 2024 01:56:58 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4cf1ed5db581f518e5a7a59100d358115e5817553178b09ecf022d2b8ec8f7`  
		Last Modified: Thu, 24 Oct 2024 01:56:58 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1479-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7cb1a45eb844897b21fbd6445ba9a73099bffb94a252123d3014a0ff883f5372
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5146047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6e4011e3dbcd14166250aa82afa2e0b89cf9c44058c9881c37f2f12fde08b7`

```dockerfile
```

-	Layers:
	-	`sha256:180f8b786e33a5111d6aa43b46d6972af549ac671a96799e27999b52d13bd6d0`  
		Last Modified: Thu, 24 Oct 2024 01:56:59 GMT  
		Size: 5.1 MB (5130329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c771078377fc2a6b42160dc9424bbff7800fd0970d530d3ad5b5d4ec2a59add`  
		Last Modified: Thu, 24 Oct 2024 01:56:58 GMT  
		Size: 15.7 KB (15718 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-1.12.0.1479-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:77a16df50a67d8d4b93f2ad0f41f9fee6e7360cad9e09bcb9fe594ccb897bb6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.4 MB (252402667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4885cbc3aff22cc44802302235818a398896afa4d6e02af898151ae7d52e4dc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef34680c3ee0cb00936471ae2c979a3b313bd7bb6fd8b2e8a4124061a483fef`  
		Last Modified: Thu, 17 Oct 2024 08:31:05 GMT  
		Size: 163.3 MB (163252839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e646fc2ccb4d95c746d3377c4bc568fd7558f45aca47d22a9d4c8414ddf80027`  
		Last Modified: Thu, 17 Oct 2024 08:34:59 GMT  
		Size: 59.1 MB (59073032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f613fe3b7e759b31ff574545b3cc9f38d75f65ac367f819077a9c47e2f99ed3c`  
		Last Modified: Thu, 17 Oct 2024 08:34:58 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6e9245f855940fbcd92121e2b6fcee7011588030c3107586bc3f4ac2a5e0ed`  
		Last Modified: Thu, 17 Oct 2024 08:34:58 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1479-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6c380af601aae3d454e7d09b142d352fed7e9ba499c86d039ad73eb30afcec67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5151258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d32deeecf276ddf4f9970100f0aa0beb5a9ce57d8bafe7afa356e0acc3c6e8`

```dockerfile
```

-	Layers:
	-	`sha256:c1bf14be31e6fd6b90201f2725376002918759bf0fb79fb07cbf27594bc623b7`  
		Last Modified: Sat, 19 Oct 2024 12:23:50 GMT  
		Size: 5.1 MB (5135428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13471af6c854d07468abb86446a5c82cd41640bfd8da46b580eb86d28ebda231`  
		Last Modified: Sat, 19 Oct 2024 12:23:49 GMT  
		Size: 15.8 KB (15830 bytes)  
		MIME: application/vnd.in-toto+json
