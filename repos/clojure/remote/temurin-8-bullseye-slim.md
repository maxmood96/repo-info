## `clojure:temurin-8-bullseye-slim`

```console
$ docker pull clojure@sha256:b54ce53959dc329e310b3046f1aac7739eab25dbb234697906f6b800aca7b926
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:879dd387d0495d83dccf53ce8e4a0f45c79ed414b4a0cbb4d42e52dbe3adf0a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.0 MB (193981329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6648a5ba97b1e15efeb7bb808f9aed60f8510fa1b97818c70a0be7f730970a26`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f67a848b2a1c8ec9182cdb468a2c438d3fc3ed752db708dbaddba5e419063f`  
		Last Modified: Sat, 19 Oct 2024 02:55:28 GMT  
		Size: 103.6 MB (103611908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c22a3d55546ade124b7970507835e34eeee6104e60efb325d870bb9ae40522`  
		Last Modified: Sat, 19 Oct 2024 02:55:27 GMT  
		Size: 58.9 MB (58939976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0090bee973a59f2a143ade68850aec8a62b4c7274328f15896b4d1e18ec02ad`  
		Last Modified: Sat, 19 Oct 2024 02:55:26 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dbc16cdaf220ade075fccb280d4fc3f31870783d8e8d6df2722b4212f54e5c70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5261616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60816ed35d9e097f99f1d0d74ab71851d58a28ceacb5e4e1ea987ea3fcecbccd`

```dockerfile
```

-	Layers:
	-	`sha256:a5ecb0ae95452e3d8f44eab90994ea50b41ec83a904ec3e30033cc2ecbddf64a`  
		Last Modified: Sat, 19 Oct 2024 02:55:26 GMT  
		Size: 5.2 MB (5247486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ea9182d6afb68b6566bcc080aed1fc3ee5f039c55cd767f7bb98e2c8c40908b`  
		Last Modified: Sat, 19 Oct 2024 02:55:26 GMT  
		Size: 14.1 KB (14130 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:51797b2ac97c85d978835dac267df666ae01d753f058cf38c0e27f6f503bba6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.9 MB (191879099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17f29fa31d8e19d014d2660e3d8f3bf8e6359cef0be53a39aee5ce66443a0aa1`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feaffa0bcbc7a9d9358c92cae47bf60b7dc6453e4dcd0145711896cdaf0ce32b`  
		Last Modified: Thu, 17 Oct 2024 07:58:37 GMT  
		Size: 102.7 MB (102729275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80590cf294636247a1b4f9469377aa29914530305abcd62558b3cccd7482f820`  
		Last Modified: Thu, 17 Oct 2024 08:02:29 GMT  
		Size: 59.1 MB (59073423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084241ce2d21116ddb6703f7e3d3cfab140bcf464f9cb0d23ad893d8a1b9e9c4`  
		Last Modified: Thu, 17 Oct 2024 08:02:27 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ac3b67db0b8eda9af955755e0f34700fe2b730aa463143a9c9fd8c840a1a58a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5242242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6fed442581f585837f06fd21f57eda8d2ff1fc2bd9c500b91f7da97a71cf707`

```dockerfile
```

-	Layers:
	-	`sha256:4b42a6ee5d06c203f85dc4392bb5dabb17024cb95835e8adc7a61804d23f702f`  
		Last Modified: Thu, 17 Oct 2024 08:02:27 GMT  
		Size: 5.2 MB (5228177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de28e30eec7e4291d770e95eb2857e3836aed20f2080dce875ffb591fce57743`  
		Last Modified: Thu, 17 Oct 2024 08:02:27 GMT  
		Size: 14.1 KB (14065 bytes)  
		MIME: application/vnd.in-toto+json
