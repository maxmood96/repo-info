## `clojure:temurin-21-bullseye-slim`

```console
$ docker pull clojure@sha256:6777d3c8c09c9414bf2471161c8f6dbef9aad6619a3630e1941cc0e28f18449a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:dfb73cd49e20cdcf1431254773b883d259cbd7c7efb0853943745a8285a983b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.9 MB (246885547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4636c92f7f9827a738f5e45f656fbaa3d203c4b828de8f2ec0a7449c737666fc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2eb5be2bb7c654e920344ca8f5eaa97c50e5dc1b7fc930c68cddcd2188ae16b`  
		Last Modified: Tue, 03 Jun 2025 13:53:07 GMT  
		Size: 157.6 MB (157634456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4368107d819a703bfe26b0acaf6fac8c3c5c112b60b36d02bce6298d351c5938`  
		Last Modified: Tue, 03 Jun 2025 13:53:03 GMT  
		Size: 59.0 MB (58994113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b06b1cb71050c19de3b480ac6684461d905dc16c5c05ae11b0533823a536364`  
		Last Modified: Tue, 03 Jun 2025 13:52:58 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ff3f30fd70ffe05f23f2c1dd6750e442ab71eb7287286b93530fb175c83dd9`  
		Last Modified: Tue, 03 Jun 2025 13:52:59 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f3a73eff237f5b0f1cd817f7a1267cdc651248d5122b29d8f0645faaffbddd06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5188959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b55bae94466ef5478c0015c38257e93526bbb7ce0e5cb0321094cd2b621e2d68`

```dockerfile
```

-	Layers:
	-	`sha256:1c8147f8a6050996703bebe51e1f434f31241fda7ce347bcf2e46ad805943cfc`  
		Last Modified: Tue, 03 Jun 2025 05:16:37 GMT  
		Size: 5.2 MB (5172384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f35b0974ecc5d62bcd34001d7f58e4388da25060b84dd6e89a8bbdbabcb34b9`  
		Last Modified: Tue, 03 Jun 2025 05:16:36 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:84868826601cb8e41ae51e848785a0a95a082f506ebc4dfad46342d5e6026bc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243805037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3010a41e1735e9b9d29a0bd173e4cb5f0e3087b275d9fc2b33acda9e2709f951`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:66850c8b65c1e9c3674a722b71f8887dd317a9b257148bb1063e88d85790544f`  
		Last Modified: Tue, 03 Jun 2025 13:30:45 GMT  
		Size: 28.7 MB (28746257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c27f9d6798235ccf5e5f695d350773cf03adc77fea3cfc1049c69b79bf7dba`  
		Last Modified: Tue, 03 Jun 2025 13:32:50 GMT  
		Size: 155.9 MB (155928816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e9420a5f9ed8df5c035d1ca62ca183ae207052d1bdc424b89cb01b45151524`  
		Last Modified: Tue, 03 Jun 2025 11:00:56 GMT  
		Size: 59.1 MB (59128924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d9d31f9924011e524e2f35e39d510a8c158a4116273fdefeafbab47ed9ec99`  
		Last Modified: Tue, 03 Jun 2025 11:00:54 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e72a80061208c8cb384b948487b8f17f5eafa753b293f0396d9d12a55794f60`  
		Last Modified: Tue, 03 Jun 2025 11:00:54 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:02e929e62a9003436d2ba0b15f1a543f5613b4eae6dc4c26e469fcec1e108b60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5194857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e799d5c931dd6abb3cf3a197cc1e5863817a628b6ac5c5e3c8739528c9e25603`

```dockerfile
```

-	Layers:
	-	`sha256:22a2d740355abdb291197ec04efb14a18d9fdd0dd4826c0052b76b0f42fbe552`  
		Last Modified: Tue, 03 Jun 2025 18:39:02 GMT  
		Size: 5.2 MB (5178140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:adb5a5bea0968d30708cdbfb6398a024a573840249dd6a423ec544b5e1cff284`  
		Last Modified: Tue, 03 Jun 2025 18:39:03 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json
