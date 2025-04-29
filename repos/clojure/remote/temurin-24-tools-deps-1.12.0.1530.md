## `clojure:temurin-24-tools-deps-1.12.0.1530`

```console
$ docker pull clojure@sha256:cb3a6374c3ec9bbe605ea0209ee88a34fb2c3da3392cc8803e130fe2f353419e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-1.12.0.1530` - linux; amd64

```console
$ docker pull clojure@sha256:321c216d5bc3045e887af7042d9eeb6f40abea42ff9b931c7dd5981b37651964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 MB (219435897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab186b62e1f5cabf06936a375c59e2ded4514eee0b17b3c60c331209513cfb3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4c36b67d1e87fdfbd0a543b44f2d18a820f9d745a3020517f50f7411c1d339`  
		Last Modified: Mon, 28 Apr 2025 22:08:12 GMT  
		Size: 90.0 MB (89951978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004469d78de90c6c6cf80934baab296babccd747813a4e69c63780209e4b4bce`  
		Last Modified: Mon, 28 Apr 2025 22:08:12 GMT  
		Size: 81.0 MB (80991682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124974ae99275abc7f293c99469d2a07f300bb7a76bed21dfbc2b17bcae1984e`  
		Last Modified: Mon, 28 Apr 2025 22:08:10 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9efd428bca3e124ab4d024d464cb1aa06aa196e13f9d10405477841b543ebe`  
		Last Modified: Mon, 28 Apr 2025 22:08:10 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.0.1530` - unknown; unknown

```console
$ docker pull clojure@sha256:f86821766fb9e7dc5ab563ab461bb8f3c3cdb254fa0e53ff46ace9a21f8261ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7140304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d252796708e13cec2882bef8ead256666d06343c2631ca783c32609d767d64d9`

```dockerfile
```

-	Layers:
	-	`sha256:d27cc174e963be3d356fe399ef7c4254eeecaf960643d04fced0e3b355dcb413`  
		Last Modified: Mon, 28 Apr 2025 22:08:11 GMT  
		Size: 7.1 MB (7123806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:457b7ef4f18d2fa18fa3f6873cb797ec6e732f71bf1ad1fc277255123e3992b5`  
		Last Modified: Mon, 28 Apr 2025 22:08:10 GMT  
		Size: 16.5 KB (16498 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.0.1530` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7ead3d95221a79a260cd234528c88b8a4d40c22a78272e3a9de71fc1f4627fe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.5 MB (220538305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a7d12240bab7ce7439e33f262e1db08da2dcbbf7f0c3c75ec0ce865cc1efce`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:71daa2c787b0984bbf3b93b60686fc9fe305d28e833914019b2745ab9f36730e`  
		Last Modified: Tue, 08 Apr 2025 00:22:46 GMT  
		Size: 48.3 MB (48327469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4532fabbe7464039f3a97caa1f05b2cb98a696be1568a91203fcecc443040bf`  
		Last Modified: Wed, 23 Apr 2025 20:02:52 GMT  
		Size: 89.1 MB (89091255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97a587e934d51a6e1eae51fc23ebe4f53074639ad1f37b36a2000fe464fb13c`  
		Last Modified: Wed, 23 Apr 2025 20:06:52 GMT  
		Size: 83.1 MB (83118536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd64411febf70bd3d30804393d647dd12eb5217a537d8de999b52d72c4dc79e1`  
		Last Modified: Wed, 23 Apr 2025 20:06:50 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b1951c9e874834d0a8bd440d5e77626a7a05a26152061eeba046f900c7b34c`  
		Last Modified: Wed, 23 Apr 2025 20:06:50 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.0.1530` - unknown; unknown

```console
$ docker pull clojure@sha256:2b24cabdb791f90e83447e3da469fdc2aea998fa9194bc4865e3e8d6f46b01bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7146230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ff8733ad3c6592712e078ebc1d31242e87a02595bb97760d7e2ff6842bac939`

```dockerfile
```

-	Layers:
	-	`sha256:a9a4ff5b02b8ed07e913b01edb267d46909adf6f03a9e10bcc223eff33d42790`  
		Last Modified: Wed, 23 Apr 2025 20:06:50 GMT  
		Size: 7.1 MB (7129590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cec907bf9895192074e987f42303f3da268eb76b1debfd034a80ad536f09d50`  
		Last Modified: Wed, 23 Apr 2025 20:06:50 GMT  
		Size: 16.6 KB (16640 bytes)  
		MIME: application/vnd.in-toto+json
