## `clojure:temurin-21-tools-deps-1.12.0.1530-bullseye-slim`

```console
$ docker pull clojure@sha256:ac4dedf29ebc4d45c4caa141e6c555fca91c019f13ce400696f389446c6b6a95
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.0.1530-bullseye-slim` - linux; amd64

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
		Last Modified: Wed, 21 May 2025 22:28:05 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2eb5be2bb7c654e920344ca8f5eaa97c50e5dc1b7fc930c68cddcd2188ae16b`  
		Last Modified: Tue, 03 Jun 2025 05:16:39 GMT  
		Size: 157.6 MB (157634456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4368107d819a703bfe26b0acaf6fac8c3c5c112b60b36d02bce6298d351c5938`  
		Last Modified: Tue, 03 Jun 2025 05:16:37 GMT  
		Size: 59.0 MB (58994113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b06b1cb71050c19de3b480ac6684461d905dc16c5c05ae11b0533823a536364`  
		Last Modified: Tue, 03 Jun 2025 05:16:36 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ff3f30fd70ffe05f23f2c1dd6750e442ab71eb7287286b93530fb175c83dd9`  
		Last Modified: Tue, 03 Jun 2025 05:16:37 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1530-bullseye-slim` - unknown; unknown

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

### `clojure:temurin-21-tools-deps-1.12.0.1530-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:958648c36deb9cb606f764c72e4c737954c1d0cc51a91d2cecaef9007efaaa47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243805139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d63ee898236fbbe059274615acc1418df8325f31a8f69d4103007d9ef243e3c`
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
		Last Modified: Wed, 21 May 2025 22:28:28 GMT  
		Size: 28.7 MB (28746257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb6aafe23ee3a98ee826ee0b23fea099b9283485a0939c89bf6b8cac4331d6c`  
		Last Modified: Thu, 22 May 2025 03:12:25 GMT  
		Size: 155.9 MB (155928823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988ba3a2b6848281c71f0c313b94c582e21fcd08ae15015c9b90d34afa91036b`  
		Last Modified: Thu, 22 May 2025 08:36:19 GMT  
		Size: 59.1 MB (59129018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9345f4578922e01d7d6526eae27c278000e03424ab6a21c309ff5697543daedb`  
		Last Modified: Thu, 22 May 2025 08:36:17 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9e4855ea29aed3ca93b79118ce8309b950972ebeaffe6c93a7c3f4a8d23b757`  
		Last Modified: Thu, 22 May 2025 08:36:17 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1530-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b57bfc5363e99f6e74d56d31c0076c39fccd6b9562bf8ebbbdb3374bc11a4d06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5193258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f38254a61208064ddba86d747372e9440c700c5ce73e475efb2286f7053bc776`

```dockerfile
```

-	Layers:
	-	`sha256:ce5543b92082fcf61ab433c2543eeecf13a03df1d3b6e7bf571db50675024d01`  
		Last Modified: Thu, 22 May 2025 08:36:18 GMT  
		Size: 5.2 MB (5176544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4246d2ffad86caf3cb1ebaddd7191558d9e585b27e819cf62fc8e9a29c8cb64e`  
		Last Modified: Thu, 22 May 2025 08:36:17 GMT  
		Size: 16.7 KB (16714 bytes)  
		MIME: application/vnd.in-toto+json
