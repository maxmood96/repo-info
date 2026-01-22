## `clojure:temurin-21-tools-deps`

```console
$ docker pull clojure@sha256:e2f32dfb076e688ad24c886f83bd50894fdc4941c364331208683eab9a1782f1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-21-tools-deps` - linux; amd64

```console
$ docker pull clojure@sha256:08d2320e7d4b2c1117d84477eda15b9427139477f979f20be892dd226e06c33d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.5 MB (287454805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d5eee5eec3ee998db661c7eef62329f05ff496bc3bfcfc24d8556a5b01af37e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 01:59:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:59:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:59:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:59:46 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 01:59:46 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 02:00:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 02:00:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 02:00:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 02:00:01 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 02:00:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:40 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22de4ddb9634a174870ea6dc7c9e9c888bb954281eaae7787ea79049a45b07e2`  
		Last Modified: Fri, 16 Jan 2026 02:00:46 GMT  
		Size: 157.8 MB (157826054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec2d60a3568c7c60064bb7a06834be3135d40ca10e1360f0f168a082fbaf121`  
		Last Modified: Fri, 16 Jan 2026 02:00:39 GMT  
		Size: 81.1 MB (81146092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ad475ea759253b8a515d434f40f78dbc9bc416d87784a6cda77c89f23c3c85`  
		Last Modified: Fri, 16 Jan 2026 02:00:22 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f5534b02cba12a0a26d56c2ef68e5fc76411e740e376ce802ee04d1e0b418f`  
		Last Modified: Fri, 16 Jan 2026 02:00:23 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:425d3600715bf6cd731d47cb99727ba1b5d784dad839681a065ab288a0371ae2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7395783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb72a36c9548a9577bee9fcd7c9a22237e22f5fb967c53feaf3d16bd3f9e410a`

```dockerfile
```

-	Layers:
	-	`sha256:1e49b934ba0f96f2014f79551c07f38ae82cc48eb57778530499483ce99ed17e`  
		Last Modified: Fri, 16 Jan 2026 02:00:23 GMT  
		Size: 7.4 MB (7379321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34aa0cc59ed11601e5ba5d933b86b6c354bdea2e68b10147f600122ad07d710d`  
		Last Modified: Fri, 16 Jan 2026 02:00:22 GMT  
		Size: 16.5 KB (16462 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:47d52aaa95e9bfc127585bcc0073fb98bc490453e473c0f4a6eb5c71c2ecc8dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.6 MB (285613877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:819ab800a46ec1e5e2dbc5bf7c0daed562e15f7e9fc85b4df268142e99f4c355`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 02:04:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 02:04:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 02:04:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:04:09 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 02:04:09 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 02:04:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 02:04:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 02:04:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 02:04:25 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 02:04:25 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:34 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573233fa641cd5687a29ff489977e494c4276e5994a4d917d115034952aeff8a`  
		Last Modified: Fri, 16 Jan 2026 02:04:50 GMT  
		Size: 156.1 MB (156107636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab4b0403d2398413bbada37e57ec70ce6027295e511a81236ad65bf575ddec3`  
		Last Modified: Fri, 16 Jan 2026 02:04:49 GMT  
		Size: 81.1 MB (81139129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab6c479113a6c946954a3dc7472814b4665e00ae3577fc2c601b80006935964`  
		Last Modified: Fri, 16 Jan 2026 02:04:55 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3379d25229ffdea00d41c197a11da60e49a3736ef166d3b5dfd715af94822b`  
		Last Modified: Fri, 16 Jan 2026 02:04:46 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:8d51820d8963781653c5d553bd3a06b4b45524ef6a27e46871e08690c88250a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7401711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04df2254ce3f280daaefffcbdc4fbf9de6cf918d104fbda4ca43750321eacf11`

```dockerfile
```

-	Layers:
	-	`sha256:a3ca919c1d5b05eda2366f950774cc93ae0d6fb6ede661025796debd3d5b7442`  
		Last Modified: Fri, 16 Jan 2026 02:04:46 GMT  
		Size: 7.4 MB (7385108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43a354ca8b2183d2fe1934c254dad9685877f08b0c9b758a81a3b89fe07df97d`  
		Last Modified: Fri, 16 Jan 2026 02:04:46 GMT  
		Size: 16.6 KB (16603 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps` - linux; ppc64le

```console
$ docker pull clojure@sha256:2d2f5e247a82d8640a4733280d67b874187a9c600c10ae6d569a7d483b29583e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297258088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c5ba59a11dedd3826d235f21670ace0f5024d93acd98f815ad88ce19103aac`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 03:27:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 03:27:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 03:27:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 03:27:00 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 03:27:02 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 03:36:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 03:36:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 03:36:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 03:36:19 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 03:36:19 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7fcf9f2b462d6af06c3ad2420b999e6b092984c4723ebac480c428a5d837d3b7`  
		Last Modified: Tue, 13 Jan 2026 00:40:14 GMT  
		Size: 52.3 MB (52327376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b81e238ae58948d8dc745be1e6898b971765c75d8be7f14150f15f3e10660ba`  
		Last Modified: Fri, 16 Jan 2026 03:30:07 GMT  
		Size: 157.9 MB (157942941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c07dee664ed41b60a433d7be77bda2f838fedfa20225a4bdf44c6b3a0ef70b`  
		Last Modified: Fri, 16 Jan 2026 03:37:25 GMT  
		Size: 87.0 MB (86986726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c064ace76363500ee893d56933c858892ef07effe370c08ed0b82517927d0987`  
		Last Modified: Fri, 16 Jan 2026 03:37:13 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec4fce555e452db63cfaf279e32692396690bf55efe81fe5baf30992359ceaf`  
		Last Modified: Fri, 16 Jan 2026 03:37:13 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:697c1db3710dab6bdbc8136168e952b3cf47d85e323faa98b9648e2baead1ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7401071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69a710c7fb417d684a521aa6a63d4b0ed18daf4879e357a9dd85a33dd8faf11d`

```dockerfile
```

-	Layers:
	-	`sha256:fc3f8892e4c1ff1786c547f24cdff242ec89996f4c1c5d09a2ac79c76ec48c33`  
		Last Modified: Fri, 16 Jan 2026 04:45:15 GMT  
		Size: 7.4 MB (7384549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47d581edd42406fa751565cba84f4a4856fff1bfd11d8b2fffe974c87bc2da0a`  
		Last Modified: Fri, 16 Jan 2026 04:45:16 GMT  
		Size: 16.5 KB (16522 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps` - linux; s390x

```console
$ docker pull clojure@sha256:d9cd3e4e8cc10cfacdeec0a88b689feb2a497928b8bd69b2f64bcc8853a63493
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274168707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a28b40d518a6fddc4eb4121e241e58ba5be2e73ceb79f80fe643fe35380863`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Thu, 15 Jan 2026 23:19:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 23:19:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 15 Jan 2026 23:19:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:19:49 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 15 Jan 2026 23:19:49 GMT
WORKDIR /tmp
# Thu, 15 Jan 2026 23:20:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 15 Jan 2026 23:20:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 15 Jan 2026 23:20:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 15 Jan 2026 23:20:02 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 15 Jan 2026 23:20:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:533e1723f6efd3a2dac5ef2d710062f1e6292bf061b83d41b908fe862b8922dc`  
		Last Modified: Tue, 13 Jan 2026 00:40:26 GMT  
		Size: 47.1 MB (47138430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9870218276608e18166550d6fb6c5680cebf5e7e53f9ed38d4773065c75b378a`  
		Last Modified: Thu, 15 Jan 2026 23:20:58 GMT  
		Size: 147.1 MB (147069856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:112c8d1d490fc0420276678c7c67dd17a86485341f0cc600ae62a9f823f4fd5e`  
		Last Modified: Thu, 15 Jan 2026 23:20:49 GMT  
		Size: 80.0 MB (79959380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da71835b73b47f76b6fe2ca2727a526f204266b825b114fecfe06b893bd98473`  
		Last Modified: Thu, 15 Jan 2026 23:20:30 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d769ffede83c977123f3182c22a49214b592361b55b1a1d5c5318126ab148bb3`  
		Last Modified: Thu, 15 Jan 2026 23:20:30 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:fa9d3a775613b437ac0f8abe1dfa97d306a14b308cd117dd587cd212a0871155
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7387102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15c979fef98ae891f8ed50e69401e23900f11e16dee4419ab885e3133aef9df2`

```dockerfile
```

-	Layers:
	-	`sha256:8e46e666faff381a12ec035bbedcdab8e167ec5e5a475741465f9182cccd4b50`  
		Last Modified: Fri, 16 Jan 2026 01:41:22 GMT  
		Size: 7.4 MB (7370640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c83f5ad17ee75b34e6646d10470ef4fb3cbaf8478e8226d06c6a9564988190ee`  
		Last Modified: Fri, 16 Jan 2026 01:41:23 GMT  
		Size: 16.5 KB (16462 bytes)  
		MIME: application/vnd.in-toto+json
