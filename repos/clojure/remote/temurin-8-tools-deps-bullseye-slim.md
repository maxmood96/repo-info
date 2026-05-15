## `clojure:temurin-8-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:3d417f6bff38eacd0e3a98007077cfba15e6687eb2439e6f45495d15921f8343
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5acb7ecc80c10d1a9045f2d2318a53bdb9cfda0530b5d6e3f4842c3adb5560e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144647817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8b9ce41bb8e8f525feb22b27be268186358ed75e44199231f201c661c0fba55`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Fri, 15 May 2026 20:13:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:13:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:13:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:13:02 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:13:02 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:13:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:13:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:13:16 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:77e30ef52aeb52d8466baf0f50b54ed2fc0b421f44c49e5bf93682b27110f4d3`  
		Last Modified: Fri, 08 May 2026 18:22:59 GMT  
		Size: 30.3 MB (30257958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ee8aa26056fe0f6c56e49e5a0b788181fdad476c68cfc92e8e190e3d723a5c`  
		Last Modified: Fri, 15 May 2026 20:13:34 GMT  
		Size: 55.2 MB (55198722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8292a14faf48b441134a1f69f346d534e94bc52f2c625739600c92ac01733eb2`  
		Last Modified: Fri, 15 May 2026 20:13:34 GMT  
		Size: 59.2 MB (59190489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fefedd24d9ebfbf6647dcc2c97ee09ed8148260e56a536110c63773e215b8b8f`  
		Last Modified: Fri, 15 May 2026 20:13:31 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:39cfaefb978531e261cbbe119b0694ba13f31fee1e499cbe6cb5a26f9c36f834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5455440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9fbbd2e031c6d5e7acae195db68bff6d25fa302f4343ebdcd475f505bcc43af`

```dockerfile
```

-	Layers:
	-	`sha256:1090d5dc410369cb9e8ca66e2bab9da344bda5c26dc5bc48ef0289c83f505f7d`  
		Last Modified: Fri, 15 May 2026 20:13:31 GMT  
		Size: 5.4 MB (5441038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fd249763c66497a22777cbfd2500cc12fd78ac70d39c043a97b5ae159c0e842`  
		Last Modified: Fri, 15 May 2026 20:13:31 GMT  
		Size: 14.4 KB (14402 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:40eb81bbf2a6f83bbc9ce565020a7815a236cee547c6bf70e66976849ff63b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.4 MB (142375956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:652d857fc4324e21484a988667b100d2a5b2587408c8d52cac1ac9eeed9da2c0`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 15 May 2026 20:13:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:13:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:13:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:13:01 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:13:01 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:13:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:13:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:13:15 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ab0f13d792ff9100407906fb422a0b62a8b437abde4c245e03f0366814be9aae`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 28.7 MB (28742591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853f3f4c625e53b71c1c35796f613f6b4cac3473f6d89a37cb50288cc07f2e56`  
		Last Modified: Fri, 15 May 2026 20:13:32 GMT  
		Size: 54.3 MB (54272927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f01ba4f9a43eebad8684f3b5a16627496c532217c512e7383ab6a4e5e07fac`  
		Last Modified: Fri, 15 May 2026 20:13:32 GMT  
		Size: 59.4 MB (59359790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f25de6068a1407df998b5c33cba615435c504a55bfd19c23af2baf82e64e82`  
		Last Modified: Fri, 15 May 2026 20:13:29 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a398125922924cd4f6ae3f11aafcf4fad7762bafdcba3be13c1106298825f20f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5461990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64319fbc6269dd54863960049c541bfb53b9bc152f7411b11bd263c16614e09b`

```dockerfile
```

-	Layers:
	-	`sha256:0304b22b6e4bd1bd8a11fa29849e6f68eb82d63ef83060fdcfdeb91cec3ee8be`  
		Last Modified: Fri, 15 May 2026 20:13:29 GMT  
		Size: 5.4 MB (5447470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe9e7d421f0341cef39cc78f7544d92efd4150ab888311975a8d18feb27715d2`  
		Last Modified: Fri, 15 May 2026 20:13:29 GMT  
		Size: 14.5 KB (14520 bytes)  
		MIME: application/vnd.in-toto+json
