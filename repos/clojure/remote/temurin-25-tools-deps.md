## `clojure:temurin-25-tools-deps`

```console
$ docker pull clojure@sha256:dbafb8185284b90f5f4ed820b074e0df97b2e0d7f92a74c839a0174a72914446
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

### `clojure:temurin-25-tools-deps` - linux; amd64

```console
$ docker pull clojure@sha256:eee4b16cf49e495097dc87e6989f4a95f65fca3894d5fb3f8f342f2c32c30efc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.3 MB (222278012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:317ec7d7b9e9c252028e6236147942c2d6190bdd48896de62b55d1033bf07a21`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 15 May 2026 20:15:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:15:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:15:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:15:40 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:15:40 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:15:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:15:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:15:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:15:55 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:15:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85285b5d9c63a28459129da04f49f48f6674eb92f19f55b93dbd03ab82d12a9`  
		Last Modified: Fri, 15 May 2026 20:16:21 GMT  
		Size: 92.6 MB (92574585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad13ef96969171a8fe67240cb67447e167192529432ccac1cc76bf1999a74b1`  
		Last Modified: Fri, 15 May 2026 20:16:18 GMT  
		Size: 81.2 MB (81213707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d742dce6ac4e46e1def0227f7c8c28eca28e40cece801b7f4ce5b16fb72e2d`  
		Last Modified: Fri, 15 May 2026 20:16:14 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca21bb1ce8f6a16f48cffe332e5d7a3ea22aefdeeaa0ae001cecff7f635c7a96`  
		Last Modified: Fri, 15 May 2026 20:16:14 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:080bb55d2cee9ba9074572cec920038b72f14ae2b0c25973cf41f49fb78c6f3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7366246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11813919c64581a78facb81d5aa548a99851f97af34e92a8757af0cc361f062c`

```dockerfile
```

-	Layers:
	-	`sha256:8633b32bc58a6b46310b570f8da4b691ea5f5468b6ef174e0744e9f2983d122b`  
		Last Modified: Fri, 15 May 2026 20:16:15 GMT  
		Size: 7.3 MB (7348321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa243709933a055cf75ca7d2a9f19dce96c09805ee435c776889a07d00508a57`  
		Last Modified: Fri, 15 May 2026 20:16:14 GMT  
		Size: 17.9 KB (17925 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:53ff4d40123c78dd30fd42c288ed4f369513700679cb258ab445e5cf016d7573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 MB (221111576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c34427dad8487aad726cd4c2e599fa2e28450ae952d0ae5a2c161cfd51385da2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 15 May 2026 20:16:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:16:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:16:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:16:02 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:16:02 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:16:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:16:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:16:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:16:17 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:16:17 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05ac32ab693cde453d49d319a678902d016d3f4e7632d27dc2ee646496e4914`  
		Last Modified: Fri, 15 May 2026 20:16:39 GMT  
		Size: 91.5 MB (91542257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f9b81640ef5342f72a4505f9f89f6a5b04a3bb421cff5c5576b59d35f5a6f6`  
		Last Modified: Fri, 15 May 2026 20:16:38 GMT  
		Size: 81.2 MB (81195123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9c4fbfbacee7448dc290f01562412b9fcbea7b114133ee081f759df6c06b58`  
		Last Modified: Fri, 15 May 2026 20:16:36 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754967bf45be8e1a090abbf344fe307c6bdde8c874d36b000934d9d207069e8d`  
		Last Modified: Fri, 15 May 2026 20:16:36 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:291deec199ac955021f9d009ce0fc7d5e4add274b45907e19ef54df927d1346f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7372268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da704c761a3e091cd894486e20ca9129b6f2ccd9e5e02ce7eede4945bc54dc69`

```dockerfile
```

-	Layers:
	-	`sha256:aedd079a02b9c268c8036661d73011f01e02f5c2ae74649657cdea87245f3eef`  
		Last Modified: Fri, 15 May 2026 20:16:36 GMT  
		Size: 7.4 MB (7354153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b841a59e7af712781eff03305cf3bbb4fc76092e6cbd06a84dbdc17c89f9fb6`  
		Last Modified: Fri, 15 May 2026 20:16:36 GMT  
		Size: 18.1 KB (18115 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps` - linux; ppc64le

```console
$ docker pull clojure@sha256:43cf5fb9c3dd34de7e644de5770995a048b0cc73145e00ad503655bad857e740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231285146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:938e2bce0c55b4df22fc364829046c5a176972c530acc037c0b0462e9f303dab`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Sat, 09 May 2026 02:18:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:18:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:18:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:18:51 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Sat, 09 May 2026 02:18:51 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:31:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:31:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:31:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:31:31 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:31:31 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:30ef9f53c997c6c1f1ab8f4cc559b32d9206d169c54ad5a0f0363076708fffef`  
		Last Modified: Fri, 08 May 2026 19:44:07 GMT  
		Size: 52.3 MB (52336787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5de956b7a11284f1a158aa4d174299365ba072baa5eadc5c41d537c7ba7509c`  
		Last Modified: Sat, 09 May 2026 02:20:31 GMT  
		Size: 91.9 MB (91914029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a131bf079ca5d3007c0def241264e6aa497a41fc7dd6bd941144d6e136728293`  
		Last Modified: Fri, 15 May 2026 20:32:09 GMT  
		Size: 87.0 MB (87033283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e94472b23a8c063a2f313b86d8ce097895d59ec00da43551cb97bba61a620f7`  
		Last Modified: Fri, 15 May 2026 20:32:05 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96fce57370e8a543b19badb0f6d46debfc70803c265634324912d0cd00d5022`  
		Last Modified: Fri, 15 May 2026 20:32:05 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:db3c156f51789308c44571412b4d667508f2ff7c242b9fed12dcfada833cac9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7353941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9332883e84b39fba57fea3de59da82a66a6434f78631b65fc6e9d1b51cee3282`

```dockerfile
```

-	Layers:
	-	`sha256:93ce6e9d761e0f59c34b9fb73b687d8cffaad1b5631ab8e70d52aa06ac0ac97d`  
		Last Modified: Fri, 15 May 2026 20:32:05 GMT  
		Size: 7.3 MB (7336885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae9516dd7ef75d59c080b4a9052db089cab6225cba5b91b548dec82df3ffcb75`  
		Last Modified: Fri, 15 May 2026 20:32:05 GMT  
		Size: 17.1 KB (17056 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps` - linux; s390x

```console
$ docker pull clojure@sha256:4b6b59d2f35957c79bf8b9563202edbd9520d21b8714139299cb341c29765647
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.6 MB (215595595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ca67604ab118745dda7ba877fbe0867f10afabbf6f2fe70e69a7415054edb3d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 23:37:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:37:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:37:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:37:14 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Thu, 14 May 2026 23:37:14 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:32:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:32:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:32:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:32:51 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:32:51 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:124dbe049873037f973f01d877ec004bf4cd3ce5723d0b8f2067c58ad98137d6`  
		Last Modified: Fri, 08 May 2026 18:27:29 GMT  
		Size: 47.1 MB (47148023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:919ff6944cfdfe171e630be33be41e61c43d3607140de9849e84caf428ea01ef`  
		Last Modified: Thu, 14 May 2026 23:37:55 GMT  
		Size: 88.4 MB (88420336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3fa39aa79f327c6a617048d89dbf51f4e34894f6b5bcd52e2898e4e1b4b881`  
		Last Modified: Fri, 15 May 2026 20:33:54 GMT  
		Size: 80.0 MB (80026191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ea24260ed65d1b3017834251dafeb0a1d431662b42cbae9b9640daac36afeb`  
		Last Modified: Fri, 15 May 2026 20:33:49 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2299353cfd7d753993c8d5ae8eef1c461b94fcd8b8a7e228b0d197173817167a`  
		Last Modified: Fri, 15 May 2026 20:33:50 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:a0c16fdb4830af2fb20239f12fe33928faadee98574e95c0432afd649915084f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7341174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1adbf0baf283cd3e99991ba3bdb69d45aaaf11b1728144bc9dc3d485a88b3251`

```dockerfile
```

-	Layers:
	-	`sha256:1e0557b337423503adec589676e127589965edbad8c99f5f8c97530e91b55d7e`  
		Last Modified: Fri, 15 May 2026 20:33:50 GMT  
		Size: 7.3 MB (7324202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4a39fd25c4961ee0d26264613a226f99500996fc765d01db0d9ae6fb468db4e`  
		Last Modified: Fri, 15 May 2026 20:33:49 GMT  
		Size: 17.0 KB (16972 bytes)  
		MIME: application/vnd.in-toto+json
