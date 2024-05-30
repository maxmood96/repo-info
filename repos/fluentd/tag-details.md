<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `fluentd`

-	[`fluentd:latest`](#fluentdlatest)
-	[`fluentd:v1.16-1`](#fluentdv116-1)
-	[`fluentd:v1.16-debian-1`](#fluentdv116-debian-1)
-	[`fluentd:v1.16.2-1.1`](#fluentdv1162-11)
-	[`fluentd:v1.16.2-debian-1.1`](#fluentdv1162-debian-11)

## `fluentd:latest`

```console
$ docker pull fluentd@sha256:6b4f3d80b3725fea379d57f9822a7091ffb211c9bfa5a3b136f7980328a44d8e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `fluentd:latest` - linux; amd64

```console
$ docker pull fluentd@sha256:26b29f21337c7f5c8146af49cce693c050861b6836d7c70a8f3a23734269e096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25125598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:272c24aaee9585f5ed6d9f3ad8649eaad5d43f0ce7e064472df514cd4404a901`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["/bin/sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 20 Sep 2023 09:43:58 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LD_PRELOAD=
# Wed, 20 Sep 2023 09:43:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 Sep 2023 09:43:58 GMT
USER fluent
# Wed, 20 Sep 2023 09:43:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c8dba7c1c75961a92b91aceecd94e73abba27b2da6976d0e0d84814509921e0`  
		Last Modified: Fri, 15 Mar 2024 23:56:16 GMT  
		Size: 21.7 MB (21744026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db926b3fe81aeeac5c07345b3c652ee349382380a8a00f2b471148c75798e2c`  
		Last Modified: Fri, 15 Mar 2024 23:56:16 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7522d0ca132649fa7268473950b6192b953a533074e8f590fbfc41eb92429e`  
		Last Modified: Fri, 15 Mar 2024 23:56:16 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f3814a6386f45a8a8ddf87ada26421082bed18ab60d72481982ea9d4dc91bab`  
		Last Modified: Fri, 15 Mar 2024 23:56:16 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:662cd3ea6d300c50acf80526616292adb23693bf3a6cc716928122ca72336026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **930.6 KB (930571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0bf0466b714fa08034af61a95b5d5b1f7c00fad14247d416929a1595c7b5546`

```dockerfile
```

-	Layers:
	-	`sha256:286d93c0f65e2ab05b300620b64cc51c1a488f3f8230fb6cbbe7c7ab2e66d5fc`  
		Last Modified: Fri, 15 Mar 2024 23:56:16 GMT  
		Size: 916.6 KB (916643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c078cf2290cddae0f2ef056fb8643e631243b642884060b46f486ae3741ec10d`  
		Last Modified: Fri, 15 Mar 2024 23:56:16 GMT  
		Size: 13.9 KB (13928 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:73163edfd7c0959532d9f766237a7ee2da4786eb2d06984e4f9353f8a6faa267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23817603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1a1f700f6d50819040b833597ce4f7fde18bb2bd057ae1dee11024bd45d04d1`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:ef699a4b52d87def9be5a058091005e5e3f0bb9fb7bf5c9fe3053ba85d79d7af in / 
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["/bin/sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 20 Sep 2023 09:43:58 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LD_PRELOAD=
# Wed, 20 Sep 2023 09:43:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 Sep 2023 09:43:58 GMT
USER fluent
# Wed, 20 Sep 2023 09:43:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:dded572f39df01b407585bbbda3ae89a2d14042e68184c8b3f6af6ac7fe5b86b`  
		Last Modified: Fri, 26 Jan 2024 23:50:01 GMT  
		Size: 3.1 MB (3113120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f547f874add8fb3d93680c430c734a4af93bb7a10a89a4b50d3e3f7542794f83`  
		Last Modified: Tue, 19 Mar 2024 11:23:21 GMT  
		Size: 20.7 MB (20702315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1da3239e5edc67c8b16bcfac0547b3192ca9c72d6ff4c2b70a75c1fc603b92a`  
		Last Modified: Tue, 19 Mar 2024 11:23:20 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a0ef6f4a0295b63760a3bf7374a5a284f8a638ed93daffbd5a45cce75ef8002`  
		Last Modified: Tue, 19 Mar 2024 11:23:20 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8a30a4dc6ad2b3c259aa977fb0c682c830f7378b30ff706598e1cdcaf9f60b`  
		Last Modified: Tue, 19 Mar 2024 11:23:20 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:6bb6c873d1ddaad02174684e6849c64140e7ce2d8c7a265eb7141c8cb14847be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 KB (13622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:147d0ecc047ffef9cf0cd8d4b10a6c0e4476c3e815452f8f4705ab277271275d`

```dockerfile
```

-	Layers:
	-	`sha256:0f24dffc28c7dc5e34e7312399eda20f9fa8901299fe30407fe1e041073dbb17`  
		Last Modified: Tue, 19 Mar 2024 11:23:20 GMT  
		Size: 13.6 KB (13622 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:9363788cb19d64dcb46eff4b4e5fedfee5bf2e5b040b653ae5930ff27f4e3fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24600146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca741c0cf2897fc408af0ab5f7f500556ae90b9a8293eaeefd60d438c859160d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:c3b6b575eb741f914ec12bd4df43de0cb044a1f2bae7ff15d176e49b5986d903 in / 
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["/bin/sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 20 Sep 2023 09:43:58 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LD_PRELOAD=
# Wed, 20 Sep 2023 09:43:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 Sep 2023 09:43:58 GMT
USER fluent
# Wed, 20 Sep 2023 09:43:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:5385a9a590c3e2872b3ed27554a56fb7ce544c694b41b9b95d70fa86f30b0566`  
		Last Modified: Fri, 26 Jan 2024 23:45:40 GMT  
		Size: 3.3 MB (3258283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91a154538f64991567fc18bd89359c3de3b13651eb79946f1f90b1412e8a6e70`  
		Last Modified: Sat, 16 Mar 2024 17:13:59 GMT  
		Size: 21.3 MB (21339698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9742b74de05dea377e49b47eae37debf6dcfe311b8e8ea9b6ffa75162c074407`  
		Last Modified: Sat, 16 Mar 2024 17:13:58 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553a1c29561145339686a65a76b90eeb345ffe79009291f1fa5b4364956d1643`  
		Last Modified: Sat, 16 Mar 2024 17:13:58 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f161510f8c1addd3cd39b60f67ed679b60dbe064d6629e91b8e6f8a82c0f39f6`  
		Last Modified: Sat, 16 Mar 2024 17:13:58 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:56405b84332edf74042515da848e8660b90d2221105bfc6c83732d51c443d2cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **930.5 KB (930517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4b60dbcdbe9c5fbdbc9c892d33e40d9d7479d5dc2097cff4f79a3019d7a759`

```dockerfile
```

-	Layers:
	-	`sha256:636b6f7ff9b943ce12db4f5d9172f89bce1a857ce9916ea83a53d06fba302d80`  
		Last Modified: Sat, 16 Mar 2024 17:13:58 GMT  
		Size: 916.7 KB (916749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc98a63a414011ab6ef76a74fcc0e91f38597c30113820286b6b17dfe722ef4f`  
		Last Modified: Sat, 16 Mar 2024 17:13:58 GMT  
		Size: 13.8 KB (13768 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; 386

```console
$ docker pull fluentd@sha256:87556a0eaac45cada6bcd15d537c2c843a6b5d6eaab7ff21349bbe357f925783
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 MB (24395126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:005963481600010f014cf4524e59bf2fe49b147db3517ebe8239b5485c9940c0`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:a7d49c3d7c0292c69f1dade47c5e95e3980c9005bd8cd9ba335627e45e225970 in / 
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["/bin/sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 20 Sep 2023 09:43:58 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LD_PRELOAD=
# Wed, 20 Sep 2023 09:43:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 Sep 2023 09:43:58 GMT
USER fluent
# Wed, 20 Sep 2023 09:43:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:db0c825f4043b16c67d2ecf8030106d2093189b8461779ac49e7c6392a532a13`  
		Last Modified: Sat, 27 Jan 2024 00:39:09 GMT  
		Size: 3.4 MB (3415178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4148a3eac4aaa35790a698ee73a2005a7d4df10da2354cf9fa759c0eb46ca47b`  
		Last Modified: Fri, 15 Mar 2024 23:57:14 GMT  
		Size: 21.0 MB (20977783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd070dc9801a5c9070bc08b77174032a64b0d54af134daa94b6c9334f494ff8a`  
		Last Modified: Fri, 15 Mar 2024 23:57:14 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2057e5a99aa6aeff7497b97ee27d6efbec3c52dfe47cc7af5a9905039df2de28`  
		Last Modified: Fri, 15 Mar 2024 23:57:14 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ebda7b1a05b51cb16303e84d4dd9f7771b388cc305515a945c5fc61428e330`  
		Last Modified: Fri, 15 Mar 2024 23:57:14 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:4d55224a5d81df950c628eb33d0b2d7e6d84709dadeae1ccfe5e15d0b2a13d46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **930.3 KB (930329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f47ab9140c9ee404624c9c1311cbee434e74896a0f571bc9b59687f3ded4e15b`

```dockerfile
```

-	Layers:
	-	`sha256:83d121be6226318aab835208721694e14f21302e43d2a6e84cf20075d1716ef8`  
		Last Modified: Fri, 15 Mar 2024 23:57:14 GMT  
		Size: 916.4 KB (916429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20a3d5c68dad5e3bbd77b7a6397529a93429c91fff02b8207dee39503225153f`  
		Last Modified: Fri, 15 Mar 2024 23:57:14 GMT  
		Size: 13.9 KB (13900 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; ppc64le

```console
$ docker pull fluentd@sha256:248f70429be97350a580c3dd40affa171909e50df799a34b04c0b4ad1f05057f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 MB (24986237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edf64deb8424068e5b471f8ccb4c4c661163865c6581af1723242b28bada930b`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:142556ae6fb4078ff8df7cd88ef4f1d91b27167561c6e93ceeee4d9a87677a22 in / 
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["/bin/sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 20 Sep 2023 09:43:58 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LD_PRELOAD=
# Wed, 20 Sep 2023 09:43:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 Sep 2023 09:43:58 GMT
USER fluent
# Wed, 20 Sep 2023 09:43:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:c4bf8831607f5d219b98313740266d85a75f3b24c83a4db919b24cc51c6da633`  
		Last Modified: Sat, 27 Jan 2024 00:28:35 GMT  
		Size: 3.4 MB (3392106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03e47551d05f6cb304609791e7d8ad952ccb21b5a6ed83090dea145c7b018ed`  
		Last Modified: Sat, 16 Mar 2024 12:08:22 GMT  
		Size: 21.6 MB (21591953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72de6bde4d31ce7857d9da696bae65f24e0bffcfe80e799c81b3f699ad54d1ae`  
		Last Modified: Sat, 16 Mar 2024 12:08:21 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb79847fa40222fe1af9b58da56f1341e2f5968348cb4de2bd61648f40466cad`  
		Last Modified: Sat, 16 Mar 2024 12:08:21 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880cdf79564ae2ad951b962bc38a099804db192b53ac5a306b85d91085a92dfd`  
		Last Modified: Sat, 16 Mar 2024 12:08:22 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:30a7543e9d7d9ecf7c7501236f8c8ddd79cd95aff5077441f6c0959f40f39e8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **929.0 KB (928998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76046f30be09378029125947bd103ffc56739ca94aca293ecf1679bf77f548d8`

```dockerfile
```

-	Layers:
	-	`sha256:2cd974dba05947f7103ee5683fe11e2c845b46fcbcfb0050d3a29fa14c6f8e28`  
		Last Modified: Sat, 16 Mar 2024 12:08:22 GMT  
		Size: 915.2 KB (915202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a871f6c06d9c14af03812268dd28e70ed1962db7dbbaa1c1bfbdc81fec76ff4e`  
		Last Modified: Sat, 16 Mar 2024 12:08:22 GMT  
		Size: 13.8 KB (13796 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; s390x

```console
$ docker pull fluentd@sha256:6a0204127ede777d74bea25d0ca72427d2173f4ec04699b87efb14ac002a33c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 MB (24350319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33acaa2070b8b267873becf367d00fb2619763992fad4d7e4afdcf47891483f5`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:332dae9ac04a5dae7353ca7443ee80390b5d93185e9dbde064b470357abc4534 in / 
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["/bin/sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 20 Sep 2023 09:43:58 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LD_PRELOAD=
# Wed, 20 Sep 2023 09:43:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 Sep 2023 09:43:58 GMT
USER fluent
# Wed, 20 Sep 2023 09:43:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:5d54cb3c0670dbeb16e4b7f6005aab36368f0ce33a7cacf5d24d1e62c4618c17`  
		Last Modified: Sat, 27 Jan 2024 00:43:35 GMT  
		Size: 3.2 MB (3176530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd53472e76590c2a8618e674bf6813eadbfafad5b1d0cff6a09ad626b7443db`  
		Last Modified: Sun, 17 Mar 2024 08:52:35 GMT  
		Size: 21.2 MB (21171623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351c9d6d4b6fa9e0747a866e3d4c3e7142b4659bc8438db24b6e288328e99dd2`  
		Last Modified: Sun, 17 Mar 2024 08:52:35 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303f4ceea1ada774bdd6797ffcf69f182bd83761ae22a5699a7e8f3b42bbc35e`  
		Last Modified: Sun, 17 Mar 2024 08:52:35 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85afb89f01c408e989aef554ee040bda1cddebb2aa47827c705ae5a8feecc215`  
		Last Modified: Sun, 17 Mar 2024 08:52:35 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:55d6196eef0ac6d020eb8e2606a7c38b7923d101f535443d91aa29b7df4a1797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **928.5 KB (928519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad92e6306f8d4bedde0e8df286a52d801c631b190f8b8eb2685eb2b4cc95c131`

```dockerfile
```

-	Layers:
	-	`sha256:c9051913d09d39474d3c99c5c8aa10021e9da9f5b9e3e7fad5740d2e1f0a454f`  
		Last Modified: Sun, 17 Mar 2024 08:52:35 GMT  
		Size: 914.6 KB (914592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82ef110b9a4885025231c108e75ef437e47b66812ccfde0dc8e81409bdd9822d`  
		Last Modified: Sun, 17 Mar 2024 08:52:34 GMT  
		Size: 13.9 KB (13927 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16-1`

```console
$ docker pull fluentd@sha256:6b4f3d80b3725fea379d57f9822a7091ffb211c9bfa5a3b136f7980328a44d8e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `fluentd:v1.16-1` - linux; amd64

```console
$ docker pull fluentd@sha256:26b29f21337c7f5c8146af49cce693c050861b6836d7c70a8f3a23734269e096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25125598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:272c24aaee9585f5ed6d9f3ad8649eaad5d43f0ce7e064472df514cd4404a901`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["/bin/sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 20 Sep 2023 09:43:58 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LD_PRELOAD=
# Wed, 20 Sep 2023 09:43:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 Sep 2023 09:43:58 GMT
USER fluent
# Wed, 20 Sep 2023 09:43:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c8dba7c1c75961a92b91aceecd94e73abba27b2da6976d0e0d84814509921e0`  
		Last Modified: Fri, 15 Mar 2024 23:56:16 GMT  
		Size: 21.7 MB (21744026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db926b3fe81aeeac5c07345b3c652ee349382380a8a00f2b471148c75798e2c`  
		Last Modified: Fri, 15 Mar 2024 23:56:16 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7522d0ca132649fa7268473950b6192b953a533074e8f590fbfc41eb92429e`  
		Last Modified: Fri, 15 Mar 2024 23:56:16 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f3814a6386f45a8a8ddf87ada26421082bed18ab60d72481982ea9d4dc91bab`  
		Last Modified: Fri, 15 Mar 2024 23:56:16 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:662cd3ea6d300c50acf80526616292adb23693bf3a6cc716928122ca72336026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **930.6 KB (930571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0bf0466b714fa08034af61a95b5d5b1f7c00fad14247d416929a1595c7b5546`

```dockerfile
```

-	Layers:
	-	`sha256:286d93c0f65e2ab05b300620b64cc51c1a488f3f8230fb6cbbe7c7ab2e66d5fc`  
		Last Modified: Fri, 15 Mar 2024 23:56:16 GMT  
		Size: 916.6 KB (916643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c078cf2290cddae0f2ef056fb8643e631243b642884060b46f486ae3741ec10d`  
		Last Modified: Fri, 15 Mar 2024 23:56:16 GMT  
		Size: 13.9 KB (13928 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-1` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:73163edfd7c0959532d9f766237a7ee2da4786eb2d06984e4f9353f8a6faa267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23817603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1a1f700f6d50819040b833597ce4f7fde18bb2bd057ae1dee11024bd45d04d1`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:ef699a4b52d87def9be5a058091005e5e3f0bb9fb7bf5c9fe3053ba85d79d7af in / 
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["/bin/sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 20 Sep 2023 09:43:58 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LD_PRELOAD=
# Wed, 20 Sep 2023 09:43:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 Sep 2023 09:43:58 GMT
USER fluent
# Wed, 20 Sep 2023 09:43:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:dded572f39df01b407585bbbda3ae89a2d14042e68184c8b3f6af6ac7fe5b86b`  
		Last Modified: Fri, 26 Jan 2024 23:50:01 GMT  
		Size: 3.1 MB (3113120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f547f874add8fb3d93680c430c734a4af93bb7a10a89a4b50d3e3f7542794f83`  
		Last Modified: Tue, 19 Mar 2024 11:23:21 GMT  
		Size: 20.7 MB (20702315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1da3239e5edc67c8b16bcfac0547b3192ca9c72d6ff4c2b70a75c1fc603b92a`  
		Last Modified: Tue, 19 Mar 2024 11:23:20 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a0ef6f4a0295b63760a3bf7374a5a284f8a638ed93daffbd5a45cce75ef8002`  
		Last Modified: Tue, 19 Mar 2024 11:23:20 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8a30a4dc6ad2b3c259aa977fb0c682c830f7378b30ff706598e1cdcaf9f60b`  
		Last Modified: Tue, 19 Mar 2024 11:23:20 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:6bb6c873d1ddaad02174684e6849c64140e7ce2d8c7a265eb7141c8cb14847be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 KB (13622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:147d0ecc047ffef9cf0cd8d4b10a6c0e4476c3e815452f8f4705ab277271275d`

```dockerfile
```

-	Layers:
	-	`sha256:0f24dffc28c7dc5e34e7312399eda20f9fa8901299fe30407fe1e041073dbb17`  
		Last Modified: Tue, 19 Mar 2024 11:23:20 GMT  
		Size: 13.6 KB (13622 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:9363788cb19d64dcb46eff4b4e5fedfee5bf2e5b040b653ae5930ff27f4e3fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24600146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca741c0cf2897fc408af0ab5f7f500556ae90b9a8293eaeefd60d438c859160d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:c3b6b575eb741f914ec12bd4df43de0cb044a1f2bae7ff15d176e49b5986d903 in / 
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["/bin/sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 20 Sep 2023 09:43:58 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LD_PRELOAD=
# Wed, 20 Sep 2023 09:43:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 Sep 2023 09:43:58 GMT
USER fluent
# Wed, 20 Sep 2023 09:43:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:5385a9a590c3e2872b3ed27554a56fb7ce544c694b41b9b95d70fa86f30b0566`  
		Last Modified: Fri, 26 Jan 2024 23:45:40 GMT  
		Size: 3.3 MB (3258283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91a154538f64991567fc18bd89359c3de3b13651eb79946f1f90b1412e8a6e70`  
		Last Modified: Sat, 16 Mar 2024 17:13:59 GMT  
		Size: 21.3 MB (21339698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9742b74de05dea377e49b47eae37debf6dcfe311b8e8ea9b6ffa75162c074407`  
		Last Modified: Sat, 16 Mar 2024 17:13:58 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553a1c29561145339686a65a76b90eeb345ffe79009291f1fa5b4364956d1643`  
		Last Modified: Sat, 16 Mar 2024 17:13:58 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f161510f8c1addd3cd39b60f67ed679b60dbe064d6629e91b8e6f8a82c0f39f6`  
		Last Modified: Sat, 16 Mar 2024 17:13:58 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:56405b84332edf74042515da848e8660b90d2221105bfc6c83732d51c443d2cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **930.5 KB (930517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4b60dbcdbe9c5fbdbc9c892d33e40d9d7479d5dc2097cff4f79a3019d7a759`

```dockerfile
```

-	Layers:
	-	`sha256:636b6f7ff9b943ce12db4f5d9172f89bce1a857ce9916ea83a53d06fba302d80`  
		Last Modified: Sat, 16 Mar 2024 17:13:58 GMT  
		Size: 916.7 KB (916749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc98a63a414011ab6ef76a74fcc0e91f38597c30113820286b6b17dfe722ef4f`  
		Last Modified: Sat, 16 Mar 2024 17:13:58 GMT  
		Size: 13.8 KB (13768 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-1` - linux; 386

```console
$ docker pull fluentd@sha256:87556a0eaac45cada6bcd15d537c2c843a6b5d6eaab7ff21349bbe357f925783
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 MB (24395126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:005963481600010f014cf4524e59bf2fe49b147db3517ebe8239b5485c9940c0`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:a7d49c3d7c0292c69f1dade47c5e95e3980c9005bd8cd9ba335627e45e225970 in / 
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["/bin/sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 20 Sep 2023 09:43:58 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LD_PRELOAD=
# Wed, 20 Sep 2023 09:43:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 Sep 2023 09:43:58 GMT
USER fluent
# Wed, 20 Sep 2023 09:43:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:db0c825f4043b16c67d2ecf8030106d2093189b8461779ac49e7c6392a532a13`  
		Last Modified: Sat, 27 Jan 2024 00:39:09 GMT  
		Size: 3.4 MB (3415178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4148a3eac4aaa35790a698ee73a2005a7d4df10da2354cf9fa759c0eb46ca47b`  
		Last Modified: Fri, 15 Mar 2024 23:57:14 GMT  
		Size: 21.0 MB (20977783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd070dc9801a5c9070bc08b77174032a64b0d54af134daa94b6c9334f494ff8a`  
		Last Modified: Fri, 15 Mar 2024 23:57:14 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2057e5a99aa6aeff7497b97ee27d6efbec3c52dfe47cc7af5a9905039df2de28`  
		Last Modified: Fri, 15 Mar 2024 23:57:14 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ebda7b1a05b51cb16303e84d4dd9f7771b388cc305515a945c5fc61428e330`  
		Last Modified: Fri, 15 Mar 2024 23:57:14 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:4d55224a5d81df950c628eb33d0b2d7e6d84709dadeae1ccfe5e15d0b2a13d46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **930.3 KB (930329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f47ab9140c9ee404624c9c1311cbee434e74896a0f571bc9b59687f3ded4e15b`

```dockerfile
```

-	Layers:
	-	`sha256:83d121be6226318aab835208721694e14f21302e43d2a6e84cf20075d1716ef8`  
		Last Modified: Fri, 15 Mar 2024 23:57:14 GMT  
		Size: 916.4 KB (916429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20a3d5c68dad5e3bbd77b7a6397529a93429c91fff02b8207dee39503225153f`  
		Last Modified: Fri, 15 Mar 2024 23:57:14 GMT  
		Size: 13.9 KB (13900 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:248f70429be97350a580c3dd40affa171909e50df799a34b04c0b4ad1f05057f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 MB (24986237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edf64deb8424068e5b471f8ccb4c4c661163865c6581af1723242b28bada930b`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:142556ae6fb4078ff8df7cd88ef4f1d91b27167561c6e93ceeee4d9a87677a22 in / 
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["/bin/sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 20 Sep 2023 09:43:58 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LD_PRELOAD=
# Wed, 20 Sep 2023 09:43:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 Sep 2023 09:43:58 GMT
USER fluent
# Wed, 20 Sep 2023 09:43:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:c4bf8831607f5d219b98313740266d85a75f3b24c83a4db919b24cc51c6da633`  
		Last Modified: Sat, 27 Jan 2024 00:28:35 GMT  
		Size: 3.4 MB (3392106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03e47551d05f6cb304609791e7d8ad952ccb21b5a6ed83090dea145c7b018ed`  
		Last Modified: Sat, 16 Mar 2024 12:08:22 GMT  
		Size: 21.6 MB (21591953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72de6bde4d31ce7857d9da696bae65f24e0bffcfe80e799c81b3f699ad54d1ae`  
		Last Modified: Sat, 16 Mar 2024 12:08:21 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb79847fa40222fe1af9b58da56f1341e2f5968348cb4de2bd61648f40466cad`  
		Last Modified: Sat, 16 Mar 2024 12:08:21 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880cdf79564ae2ad951b962bc38a099804db192b53ac5a306b85d91085a92dfd`  
		Last Modified: Sat, 16 Mar 2024 12:08:22 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:30a7543e9d7d9ecf7c7501236f8c8ddd79cd95aff5077441f6c0959f40f39e8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **929.0 KB (928998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76046f30be09378029125947bd103ffc56739ca94aca293ecf1679bf77f548d8`

```dockerfile
```

-	Layers:
	-	`sha256:2cd974dba05947f7103ee5683fe11e2c845b46fcbcfb0050d3a29fa14c6f8e28`  
		Last Modified: Sat, 16 Mar 2024 12:08:22 GMT  
		Size: 915.2 KB (915202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a871f6c06d9c14af03812268dd28e70ed1962db7dbbaa1c1bfbdc81fec76ff4e`  
		Last Modified: Sat, 16 Mar 2024 12:08:22 GMT  
		Size: 13.8 KB (13796 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-1` - linux; s390x

```console
$ docker pull fluentd@sha256:6a0204127ede777d74bea25d0ca72427d2173f4ec04699b87efb14ac002a33c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 MB (24350319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33acaa2070b8b267873becf367d00fb2619763992fad4d7e4afdcf47891483f5`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:332dae9ac04a5dae7353ca7443ee80390b5d93185e9dbde064b470357abc4534 in / 
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["/bin/sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 20 Sep 2023 09:43:58 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LD_PRELOAD=
# Wed, 20 Sep 2023 09:43:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 Sep 2023 09:43:58 GMT
USER fluent
# Wed, 20 Sep 2023 09:43:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:5d54cb3c0670dbeb16e4b7f6005aab36368f0ce33a7cacf5d24d1e62c4618c17`  
		Last Modified: Sat, 27 Jan 2024 00:43:35 GMT  
		Size: 3.2 MB (3176530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd53472e76590c2a8618e674bf6813eadbfafad5b1d0cff6a09ad626b7443db`  
		Last Modified: Sun, 17 Mar 2024 08:52:35 GMT  
		Size: 21.2 MB (21171623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351c9d6d4b6fa9e0747a866e3d4c3e7142b4659bc8438db24b6e288328e99dd2`  
		Last Modified: Sun, 17 Mar 2024 08:52:35 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303f4ceea1ada774bdd6797ffcf69f182bd83761ae22a5699a7e8f3b42bbc35e`  
		Last Modified: Sun, 17 Mar 2024 08:52:35 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85afb89f01c408e989aef554ee040bda1cddebb2aa47827c705ae5a8feecc215`  
		Last Modified: Sun, 17 Mar 2024 08:52:35 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:55d6196eef0ac6d020eb8e2606a7c38b7923d101f535443d91aa29b7df4a1797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **928.5 KB (928519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad92e6306f8d4bedde0e8df286a52d801c631b190f8b8eb2685eb2b4cc95c131`

```dockerfile
```

-	Layers:
	-	`sha256:c9051913d09d39474d3c99c5c8aa10021e9da9f5b9e3e7fad5740d2e1f0a454f`  
		Last Modified: Sun, 17 Mar 2024 08:52:35 GMT  
		Size: 914.6 KB (914592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82ef110b9a4885025231c108e75ef437e47b66812ccfde0dc8e81409bdd9822d`  
		Last Modified: Sun, 17 Mar 2024 08:52:34 GMT  
		Size: 13.9 KB (13927 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16-debian-1`

```console
$ docker pull fluentd@sha256:533f5df642e8433d5c83c384497136e396d9e8be1c5d2c9b127767de3ee73509
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `fluentd:v1.16-debian-1` - linux; amd64

```console
$ docker pull fluentd@sha256:7ea25a8471c79337b6ff256d912d5593773fb5735e974c4d92fb283a8f6e3ac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101283905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c2e4c91448fb59e27d9d889166c38410db0ab5d709ea6350e028f8ff1e933b`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:43:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LANG=C.UTF-8
# Wed, 20 Sep 2023 09:43:58 GMT
ENV RUBY_VERSION=3.1.6
# Wed, 20 Sep 2023 09:43:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.1/ruby-3.1.6.tar.xz
# Wed, 20 Sep 2023 09:43:58 GMT
ENV RUBY_DOWNLOAD_SHA256=597bd1849f252d8a6863cb5d38014ac54152b508c36dca156f6356a9e63c6102
# Wed, 20 Sep 2023 09:43:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 Sep 2023 09:43:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 Sep 2023 09:43:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 09:43:58 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["irb"]
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 20 Sep 2023 09:43:58 GMT
ENV TINI_VERSION=0.18.0
# Wed, 20 Sep 2023 09:43:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 20 Sep 2023 09:43:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 Sep 2023 09:43:58 GMT
USER fluent
# Wed, 20 Sep 2023 09:43:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9082bd5a89037e709a10a4a21acfee0b84fd88a794d8e4fb0c10176f2b8293a`  
		Last Modified: Wed, 29 May 2024 23:03:55 GMT  
		Size: 9.8 MB (9815742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea461a053a2dbc652fe71eeed34571bdf8c953184ec6f1a706fe394b640615e`  
		Last Modified: Wed, 29 May 2024 23:03:54 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ab168a37ec4dfdb009b9f749b96df7fa4c3cb46aae1b60425ff80437b19e23`  
		Last Modified: Wed, 29 May 2024 23:03:55 GMT  
		Size: 32.5 MB (32467562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519e60aa436396ec421b4659295c2bf4b68d2ddce63acd84652cc579599102bc`  
		Last Modified: Wed, 29 May 2024 23:03:54 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530c9b07e5e9993f79b2adaef2281822c862b6effc8cda9df38f36390015aa7c`  
		Last Modified: Wed, 29 May 2024 23:59:12 GMT  
		Size: 27.6 MB (27563736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b9e0dcf1e7e6e633efee3014532c5a54bcd5b118f8fd0e34b1175c3e635c897`  
		Last Modified: Wed, 29 May 2024 23:59:12 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3dd8469604ccd79f343655da0ad1c374250be62e5bcc5a0d4d2ca841c62029`  
		Last Modified: Wed, 29 May 2024 23:59:12 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c142c6ff8dc368ba27db532b08ebf042e2b1a1be48f6fe434230e3e31fd373b`  
		Last Modified: Wed, 29 May 2024 23:59:12 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:745e9d3f36857caefe0a67d7308367395ddd5a5db2738750c63e913bab53127d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4121510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35260245b6107885d52a2f50236b0971025ca4a2f39ae946697608193641ab58`

```dockerfile
```

-	Layers:
	-	`sha256:9e2dc15e9046fbd9008c1557162ce3f835c1629f170ad9ef8438439132c9285d`  
		Last Modified: Wed, 29 May 2024 23:59:12 GMT  
		Size: 4.1 MB (4100445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a23bf22989b2fdff2264c8d0c57ca277d96b4c02f38425354ffd93f0b134c1ed`  
		Last Modified: Wed, 29 May 2024 23:59:12 GMT  
		Size: 21.1 KB (21065 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:fc92ea3152b0c8fe2700ad4163072613688143b2f7f84ef280f1f9b489bad004
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94804559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de59fba9727de3ece8a43a69ae8667d2b0c0c338657e9a230ece022ee052c48`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:7a63cf2b5d16adf102fbd2452be219224667c4ea55981247f398a4a867ef96c4 in / 
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:43:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LANG=C.UTF-8
# Wed, 20 Sep 2023 09:43:58 GMT
ENV RUBY_VERSION=3.1.6
# Wed, 20 Sep 2023 09:43:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.1/ruby-3.1.6.tar.xz
# Wed, 20 Sep 2023 09:43:58 GMT
ENV RUBY_DOWNLOAD_SHA256=597bd1849f252d8a6863cb5d38014ac54152b508c36dca156f6356a9e63c6102
# Wed, 20 Sep 2023 09:43:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 Sep 2023 09:43:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 Sep 2023 09:43:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 09:43:58 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["irb"]
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 20 Sep 2023 09:43:58 GMT
ENV TINI_VERSION=0.18.0
# Wed, 20 Sep 2023 09:43:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 20 Sep 2023 09:43:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 Sep 2023 09:43:58 GMT
USER fluent
# Wed, 20 Sep 2023 09:43:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:b6ea79e472ea80a508a2732ddeb0e19de51d3f0aaf8f0fd18c1cdd1c939d49de`  
		Last Modified: Tue, 14 May 2024 00:52:17 GMT  
		Size: 28.9 MB (28936721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33cbc8081ab7d7b6be84a5e608e5fd1f98691dd8a1cd02b9a291eedf4964a17d`  
		Last Modified: Wed, 29 May 2024 23:24:24 GMT  
		Size: 8.4 MB (8429217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83ddd53ec367faf472712ad792c2f294c042f57bc066e861839ccbe5b6f1069`  
		Last Modified: Wed, 29 May 2024 23:24:23 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e80bc0b2c35753df606135c4129ed1828702ca3d91ce760ab84a7ab6212307a`  
		Last Modified: Wed, 29 May 2024 23:24:25 GMT  
		Size: 31.0 MB (31016093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a57b966212874b49581cb4e64e211df8356706b7847fb5f35789626f0982d7c`  
		Last Modified: Wed, 29 May 2024 23:24:24 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66307f145e38aa0d8a4a40f17bd604c3077e1d4bfe8d1ea88ae111e99038fa96`  
		Last Modified: Thu, 30 May 2024 00:05:23 GMT  
		Size: 26.4 MB (26419604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e4661a5bb357fe29b6b84fcfba22d8c0ea435f32aefbcf073c1c1c95a147d9`  
		Last Modified: Thu, 30 May 2024 00:05:22 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1939d0b5f05f84aad8d87f37400706f43132c07623da6e23b918ba5d30be05`  
		Last Modified: Thu, 30 May 2024 00:05:22 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e7130f8cfbe0d908ad46ceec6671fb80b774d9a5971e79f38da8b329ce3322`  
		Last Modified: Thu, 30 May 2024 00:05:22 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:3f913bf0d3fb424edcae62a693306f12f6d1b2c12d782acf859d6c241d61a58f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4092828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ac8fee0c7d21191abda77720592137a7a11075246566d7b4fc9a1b58f443160`

```dockerfile
```

-	Layers:
	-	`sha256:fbd4eae738d470dc66f79d324816fd72ce57797f140e0bd3f09a4cf5fb1b3db4`  
		Last Modified: Thu, 30 May 2024 00:05:22 GMT  
		Size: 4.1 MB (4071659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c99f70914906ca3563346406ff52069f9b06b239fbd56836ab8a0e18ec8554a9`  
		Last Modified: Thu, 30 May 2024 00:05:22 GMT  
		Size: 21.2 KB (21169 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:f56e1e20f567e9455829b20c8e342a9cc07ca2dce6ba6dc22b4a6d6ce83b78e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.7 MB (91683933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:989a1123ac3fc7ef3c543316517ebc4bfc6227e9b4cea83b0b7edc4d113d178b`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:b58f353e9d2a24c2c16ae0913b28705d3ecc439d60d82b5b4982780c59aae249 in / 
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:43:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LANG=C.UTF-8
# Wed, 20 Sep 2023 09:43:58 GMT
ENV RUBY_VERSION=3.1.5
# Wed, 20 Sep 2023 09:43:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.1/ruby-3.1.5.tar.xz
# Wed, 20 Sep 2023 09:43:58 GMT
ENV RUBY_DOWNLOAD_SHA256=f9375a45bdf1cc41298558e7ac6c367f7b6cdcccf7196618b21f0886ff583b91
# Wed, 20 Sep 2023 09:43:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 Sep 2023 09:43:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 Sep 2023 09:43:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 09:43:58 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["irb"]
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 20 Sep 2023 09:43:58 GMT
ENV TINI_VERSION=0.18.0
# Wed, 20 Sep 2023 09:43:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 20 Sep 2023 09:43:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 Sep 2023 09:43:58 GMT
USER fluent
# Wed, 20 Sep 2023 09:43:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:a5c0b9604ae49509a7875b258d98493d63bdb4c1c27a70f2befa5fa4fcea1888`  
		Last Modified: Tue, 14 May 2024 01:13:30 GMT  
		Size: 26.6 MB (26594493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b2ac23e89df319720e3958b1f2d3a5fc86dfef34df01d524fc76564f5ec6858`  
		Last Modified: Tue, 14 May 2024 19:54:15 GMT  
		Size: 7.9 MB (7937129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5f1ded0e7e04ee269a1a441a15e3dcb25dec72c008121e727785185949be7f`  
		Last Modified: Tue, 14 May 2024 19:54:14 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8711b18a55f2058f9d4cf5f5145f1c65d307c48bb185356d36ab3d5df1da0578`  
		Last Modified: Tue, 14 May 2024 20:16:20 GMT  
		Size: 30.9 MB (30890606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa25f54f1918243acee6f251f389b3dceb9abf85e2c3e1e822a40742d7dd6dd`  
		Last Modified: Tue, 14 May 2024 20:16:19 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f2d15a225d8cddfa78b7ba48f475407fa3fd0ca4be7416862f4f063f0fabcd`  
		Last Modified: Wed, 15 May 2024 08:48:30 GMT  
		Size: 26.3 MB (26258784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da985258c02a7ceda7071a85fab755a831eff9097ec8dc50ab880767559c839`  
		Last Modified: Wed, 15 May 2024 08:48:29 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd1f641446a73af8575096e6b16d56f890d2b24796ce5f1b7c5b5fbc6533d62`  
		Last Modified: Wed, 15 May 2024 08:48:29 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb444b5572b53637ebb6c19d4acb946896f6d55730cb546e51f2c66aa45cf190`  
		Last Modified: Wed, 15 May 2024 08:48:29 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:618d6585f4428904935200b2afd774f2b54ed76b046a53af9192c86788a11ac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4096388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db669692a0e590e2bd9611d1b5400cce9fde931a8c842db2a05c5816b51dcd5f`

```dockerfile
```

-	Layers:
	-	`sha256:13af4ba4fa920ee05c40fabdcc002d70a359003f6a7b5f98ffc3ad26cda1f3d4`  
		Last Modified: Wed, 15 May 2024 08:48:29 GMT  
		Size: 4.1 MB (4074427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce265ce0c76a07f84c415d02c91c1998ddb9010445065d6dedf7c10924999f79`  
		Last Modified: Wed, 15 May 2024 08:48:29 GMT  
		Size: 22.0 KB (21961 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:b37b9baf78fd96ede20a219c158bb85cc70d1b9f573b2e95647f27d57537e2a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.3 MB (98312576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df277e7e81c2504353635abb1a797cde7355cf7be21b875a227b60bf8c99b2c6`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:43:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LANG=C.UTF-8
# Wed, 20 Sep 2023 09:43:58 GMT
ENV RUBY_VERSION=3.1.5
# Wed, 20 Sep 2023 09:43:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.1/ruby-3.1.5.tar.xz
# Wed, 20 Sep 2023 09:43:58 GMT
ENV RUBY_DOWNLOAD_SHA256=f9375a45bdf1cc41298558e7ac6c367f7b6cdcccf7196618b21f0886ff583b91
# Wed, 20 Sep 2023 09:43:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 Sep 2023 09:43:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 Sep 2023 09:43:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 09:43:58 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["irb"]
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 20 Sep 2023 09:43:58 GMT
ENV TINI_VERSION=0.18.0
# Wed, 20 Sep 2023 09:43:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 20 Sep 2023 09:43:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 Sep 2023 09:43:58 GMT
USER fluent
# Wed, 20 Sep 2023 09:43:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a0d9118b4abd2d5feec7b459ee3bdca44f2aef03dc342fad499ad497af4c47`  
		Last Modified: Tue, 14 May 2024 22:36:20 GMT  
		Size: 9.0 MB (9036885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da555d0f96d5a45244d417af80eeb351678c49220acfa3080a31e1d53de6fcff`  
		Last Modified: Tue, 14 May 2024 22:36:20 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488f4b09e69ab09fe12d719b25b254d37cc5c19d86ddd3383f4ff9993c15fdde`  
		Last Modified: Tue, 14 May 2024 23:35:25 GMT  
		Size: 31.8 MB (31836703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8441e3698a1ec01cede57326ce007515dd33a7b1c5ed94e9eadaa420ebf8adcb`  
		Last Modified: Tue, 14 May 2024 23:35:25 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d5fa3e7aeca62fa74dcc5af65f95cbe381a5e56b2c8aa94f29529434114224`  
		Last Modified: Wed, 15 May 2024 16:28:46 GMT  
		Size: 27.3 MB (27349151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d17cf858e4773259edc64bfa39ac59390ff0bf908e023cbef9e1baa3503421b`  
		Last Modified: Wed, 15 May 2024 16:28:45 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5cf6a208196cc026d25c432def3f865bca0488bc885d44e1b13edaa0483b6b`  
		Last Modified: Wed, 15 May 2024 16:28:45 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60e8d03118d1489980e302a46f27564c3e2f0aa53770bcf523605ae4855983c`  
		Last Modified: Wed, 15 May 2024 16:28:45 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:1faadb74443cb8d29fb2547ae3390e9bc3b1416bcae81306162ec78d074986ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4096681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add83f8a4d18b1be46149e7c8067bac31d08727b4b50fa3fb714baabbf293f54`

```dockerfile
```

-	Layers:
	-	`sha256:9499bcf28a0d3b20b89ebc0968b72f58299db84b84668757f30736995a27c0bc`  
		Last Modified: Wed, 15 May 2024 16:28:46 GMT  
		Size: 4.1 MB (4074782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b6a37df529f05a1a674708d72330c4f5f793f3f167a1dc5b1a3999d0cf9ba7b`  
		Last Modified: Wed, 15 May 2024 16:28:45 GMT  
		Size: 21.9 KB (21899 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; 386

```console
$ docker pull fluentd@sha256:2cd66687f3140602933bed40a9549c69830191664af9ce34029bafbadf704a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101698588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:855c64704bb29070d11f3939e973a3ff262a6e06b67b2855ec9f8a4e49c6adf4`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:8cc17bd8431911317f7d91df00ff305ed2f31f83f3224da64f6d7b9c38819dae in / 
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:43:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LANG=C.UTF-8
# Wed, 20 Sep 2023 09:43:58 GMT
ENV RUBY_VERSION=3.1.6
# Wed, 20 Sep 2023 09:43:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.1/ruby-3.1.6.tar.xz
# Wed, 20 Sep 2023 09:43:58 GMT
ENV RUBY_DOWNLOAD_SHA256=597bd1849f252d8a6863cb5d38014ac54152b508c36dca156f6356a9e63c6102
# Wed, 20 Sep 2023 09:43:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 Sep 2023 09:43:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 Sep 2023 09:43:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 09:43:58 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["irb"]
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 20 Sep 2023 09:43:58 GMT
ENV TINI_VERSION=0.18.0
# Wed, 20 Sep 2023 09:43:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 20 Sep 2023 09:43:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 Sep 2023 09:43:58 GMT
USER fluent
# Wed, 20 Sep 2023 09:43:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:de7432ff839295b583814dfc21a6afb18eb4e45d8144c26b1402229e5bc8105f`  
		Last Modified: Tue, 14 May 2024 00:52:45 GMT  
		Size: 32.4 MB (32424043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3a568a45828b1d1298f4d99959795046d53abb6d4d63888199208cbf741172`  
		Last Modified: Wed, 29 May 2024 23:03:58 GMT  
		Size: 11.8 MB (11791241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e97e3dd3c171d5e9fec973c4ead6b2c692d2770a7857701b085270a61f4db0`  
		Last Modified: Wed, 29 May 2024 23:03:57 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d04aed719335219282911ec2a861542ed0c99ec89013f0cc2adb69d9959696`  
		Last Modified: Wed, 29 May 2024 23:03:59 GMT  
		Size: 31.0 MB (31034408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d972742b85775ff020962d4ddc3864adee1aaf742f00c1270bef40cacfeff65`  
		Last Modified: Wed, 29 May 2024 23:03:58 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:517efb1e5ca0c4698725df3d8d41156d9185428768294a137e6ae0cfaf468348`  
		Last Modified: Wed, 29 May 2024 23:59:06 GMT  
		Size: 26.4 MB (26445972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6780445ce7f3d5c77287f446bd3a8dfbd303a36a553a6e4b2e711de394376d`  
		Last Modified: Wed, 29 May 2024 23:59:06 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6469bde1f30d98a5801181e01f1e520f9d859660e00b04ed88ab871f1bfeaaa8`  
		Last Modified: Wed, 29 May 2024 23:59:06 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a573623fb52af81da685c6d1f0c9a5ee58948bb96fe2d608292ee5dc21ee34db`  
		Last Modified: Wed, 29 May 2024 23:59:06 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:58f226a999c131152fcb6bf46313384a81117f574c2acc682fbfbe9f9dc1290f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4125699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ac51640d97fc07d4ec6d6a6a2b72e68fbdbc1c3f978f7ccc61036d99dfeb929`

```dockerfile
```

-	Layers:
	-	`sha256:a65136730f98ae64b27e2f1cd4a89958d34c14ab6132032f1bdbbc8be71d9880`  
		Last Modified: Wed, 29 May 2024 23:59:06 GMT  
		Size: 4.1 MB (4104652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63498123fe8b580ddeaf93d6a2318404badc699a70f4424aa72f5f184097f30b`  
		Last Modified: Wed, 29 May 2024 23:59:06 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:c58d402cd73a61a8719055d598c3d34030b35d5c459cbb4172aa6a18e242528d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106317383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4c86c71f1ddbeaeb57fb181709d57677a6d08399c9993b872245bbe64357ec`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:7c74907a13931bf5f38ce8642536ee05738ba9d233424998c52fc548130034b5 in / 
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:43:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LANG=C.UTF-8
# Wed, 20 Sep 2023 09:43:58 GMT
ENV RUBY_VERSION=3.1.5
# Wed, 20 Sep 2023 09:43:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.1/ruby-3.1.5.tar.xz
# Wed, 20 Sep 2023 09:43:58 GMT
ENV RUBY_DOWNLOAD_SHA256=f9375a45bdf1cc41298558e7ac6c367f7b6cdcccf7196618b21f0886ff583b91
# Wed, 20 Sep 2023 09:43:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 Sep 2023 09:43:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 Sep 2023 09:43:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 09:43:58 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["irb"]
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 20 Sep 2023 09:43:58 GMT
ENV TINI_VERSION=0.18.0
# Wed, 20 Sep 2023 09:43:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 20 Sep 2023 09:43:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 Sep 2023 09:43:58 GMT
USER fluent
# Wed, 20 Sep 2023 09:43:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:8fd45f8fa7e828bdb5dd8878febd6f367c5092a047db5f6ca094056a1b0c627c`  
		Last Modified: Tue, 14 May 2024 01:24:52 GMT  
		Size: 35.3 MB (35311159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77eaf038fe95ed309a54977b60e55f1d616cfb95ff9b10e60f7cae3eb1170ca6`  
		Last Modified: Tue, 14 May 2024 16:21:18 GMT  
		Size: 10.3 MB (10276044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0dd0072d29e123334a97df766bd98dbdbcae449a8731c89e8068d669ab561f1`  
		Last Modified: Tue, 14 May 2024 16:21:17 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d558d400b4bcf627df89f26db603f01271c88447c4cd8b8aa65f63e18e97f2`  
		Last Modified: Tue, 14 May 2024 16:35:01 GMT  
		Size: 32.7 MB (32650680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb545335c09afd49c5ab46011643532b1432001efebfc2ee1c23e9aa85b9247b`  
		Last Modified: Tue, 14 May 2024 16:35:00 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b1723c886e41a8430ac12a3ee7b7dc1e8aaf241ffaf4347f7fee5e123b38bb`  
		Last Modified: Wed, 15 May 2024 05:29:06 GMT  
		Size: 28.1 MB (28076573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6469099fe3687b027cbe49a9b54caa0298de7f35ce1969c3cc7e0cd8ab0a8b3a`  
		Last Modified: Wed, 15 May 2024 05:29:05 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19956713298118dda41b05a3ec0f484ae0c9af4f0cc30d13f3d7b09bfa72a01`  
		Last Modified: Wed, 15 May 2024 05:29:06 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e77bc938f620a386632604696f4d850114e087163e0f06e892af60a48b5e66`  
		Last Modified: Wed, 15 May 2024 05:29:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:25382af1f11d10de3b6aee6c3b36b58ad4960e2cf4f22f52e52c8617ed6e8c04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4111265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab12ea329458719a2a852b6ba98b6ddc5d90a17a6bc42b48de6ebd2b8ac5b2d`

```dockerfile
```

-	Layers:
	-	`sha256:0cead822999fda491b4c61bf54687df43deea1772278411200bbc99f97ffafd1`  
		Last Modified: Wed, 15 May 2024 05:29:05 GMT  
		Size: 4.1 MB (4089337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0aa7c95f63163520218f9067b676d23f4bfc7883428b5ef0e89a3cae83ab832b`  
		Last Modified: Wed, 15 May 2024 05:29:05 GMT  
		Size: 21.9 KB (21928 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; s390x

```console
$ docker pull fluentd@sha256:1120657de1a63464e03ff4a193e3ca9e45762eb54e15b1291ddda9bbdc7fbd6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98443866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f15088fd1c4701a9428f92106d3e4629e5daf2f63e338ca9425afacac84c83b`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:bac230200161ff0b0332af3dc90dc1aba6bdeb875d95659699251b2af4eec8dc in / 
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:43:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LANG=C.UTF-8
# Wed, 20 Sep 2023 09:43:58 GMT
ENV RUBY_VERSION=3.1.5
# Wed, 20 Sep 2023 09:43:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.1/ruby-3.1.5.tar.xz
# Wed, 20 Sep 2023 09:43:58 GMT
ENV RUBY_DOWNLOAD_SHA256=f9375a45bdf1cc41298558e7ac6c367f7b6cdcccf7196618b21f0886ff583b91
# Wed, 20 Sep 2023 09:43:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 Sep 2023 09:43:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 Sep 2023 09:43:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 09:43:58 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["irb"]
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 20 Sep 2023 09:43:58 GMT
ENV TINI_VERSION=0.18.0
# Wed, 20 Sep 2023 09:43:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 20 Sep 2023 09:43:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 Sep 2023 09:43:58 GMT
USER fluent
# Wed, 20 Sep 2023 09:43:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:14d39445de105c0a8fe00b3899e9fdab7cdfbb3ff27c8b39dd9059f3264a4841`  
		Last Modified: Tue, 14 May 2024 00:48:06 GMT  
		Size: 29.7 MB (29673656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c3fa34390dfcb4371e42b7087cc2aea1a4f78c53b90bd2236df2ac51939fcca`  
		Last Modified: Tue, 14 May 2024 23:49:14 GMT  
		Size: 8.7 MB (8656969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d975f167082b1dee6574bbada3e46d74a2ccc11f8ca7335acb5d1176e278d09a`  
		Last Modified: Tue, 14 May 2024 23:49:13 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115fde46bf9e7631e29084b296c364a52437a3a8bf81d484fb6cbed589b29f35`  
		Last Modified: Wed, 15 May 2024 00:35:30 GMT  
		Size: 32.3 MB (32299053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0ced180afb5290ebfd1648aac980679b1a5233a6d382b39688db22b84361f9`  
		Last Modified: Wed, 15 May 2024 00:35:29 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d3f5d684ec1600fafdfea3bff643c9f583db014632b3c8744a3b168b9fa6c0`  
		Last Modified: Wed, 15 May 2024 03:31:10 GMT  
		Size: 27.8 MB (27811255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ad37f60f7dad780a79d16a0790eebc7aea4f92eefd5431d37a9694fcfeac74`  
		Last Modified: Wed, 15 May 2024 03:31:09 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629fc2797ec37760927f9cf727dcb4ddef081eaa280360db13ab61faf62c8967`  
		Last Modified: Wed, 15 May 2024 03:31:09 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9367bec0ed2db3b7bd4618f3ebc5f6c8fa712eb72b835d25e484809a295cf0ac`  
		Last Modified: Wed, 15 May 2024 03:31:09 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:596c553520817882fc5ff58151c9020786097af4de2d7275c2a487b4a71e7563
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4111010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ea34d975544f1d6b509290a59ee569f844eaf05f255820939b18e90c3c88b2`

```dockerfile
```

-	Layers:
	-	`sha256:bb14a10da8944e5f08710cfd825833929f0cbc8923324a6dc079f9f27ba03854`  
		Last Modified: Wed, 15 May 2024 03:31:09 GMT  
		Size: 4.1 MB (4089122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee61cbec8ff5df433bbe16c4c3374481e1d2ba39b88aa83c60a250dc7ef8b318`  
		Last Modified: Wed, 15 May 2024 03:31:09 GMT  
		Size: 21.9 KB (21888 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16.2-1.1`

```console
$ docker pull fluentd@sha256:6b4f3d80b3725fea379d57f9822a7091ffb211c9bfa5a3b136f7980328a44d8e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `fluentd:v1.16.2-1.1` - linux; amd64

```console
$ docker pull fluentd@sha256:26b29f21337c7f5c8146af49cce693c050861b6836d7c70a8f3a23734269e096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25125598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:272c24aaee9585f5ed6d9f3ad8649eaad5d43f0ce7e064472df514cd4404a901`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["/bin/sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 20 Sep 2023 09:43:58 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LD_PRELOAD=
# Wed, 20 Sep 2023 09:43:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 Sep 2023 09:43:58 GMT
USER fluent
# Wed, 20 Sep 2023 09:43:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c8dba7c1c75961a92b91aceecd94e73abba27b2da6976d0e0d84814509921e0`  
		Last Modified: Fri, 15 Mar 2024 23:56:16 GMT  
		Size: 21.7 MB (21744026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db926b3fe81aeeac5c07345b3c652ee349382380a8a00f2b471148c75798e2c`  
		Last Modified: Fri, 15 Mar 2024 23:56:16 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7522d0ca132649fa7268473950b6192b953a533074e8f590fbfc41eb92429e`  
		Last Modified: Fri, 15 Mar 2024 23:56:16 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f3814a6386f45a8a8ddf87ada26421082bed18ab60d72481982ea9d4dc91bab`  
		Last Modified: Fri, 15 Mar 2024 23:56:16 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.2-1.1` - unknown; unknown

```console
$ docker pull fluentd@sha256:662cd3ea6d300c50acf80526616292adb23693bf3a6cc716928122ca72336026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **930.6 KB (930571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0bf0466b714fa08034af61a95b5d5b1f7c00fad14247d416929a1595c7b5546`

```dockerfile
```

-	Layers:
	-	`sha256:286d93c0f65e2ab05b300620b64cc51c1a488f3f8230fb6cbbe7c7ab2e66d5fc`  
		Last Modified: Fri, 15 Mar 2024 23:56:16 GMT  
		Size: 916.6 KB (916643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c078cf2290cddae0f2ef056fb8643e631243b642884060b46f486ae3741ec10d`  
		Last Modified: Fri, 15 Mar 2024 23:56:16 GMT  
		Size: 13.9 KB (13928 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.2-1.1` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:73163edfd7c0959532d9f766237a7ee2da4786eb2d06984e4f9353f8a6faa267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23817603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1a1f700f6d50819040b833597ce4f7fde18bb2bd057ae1dee11024bd45d04d1`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:ef699a4b52d87def9be5a058091005e5e3f0bb9fb7bf5c9fe3053ba85d79d7af in / 
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["/bin/sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 20 Sep 2023 09:43:58 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LD_PRELOAD=
# Wed, 20 Sep 2023 09:43:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 Sep 2023 09:43:58 GMT
USER fluent
# Wed, 20 Sep 2023 09:43:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:dded572f39df01b407585bbbda3ae89a2d14042e68184c8b3f6af6ac7fe5b86b`  
		Last Modified: Fri, 26 Jan 2024 23:50:01 GMT  
		Size: 3.1 MB (3113120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f547f874add8fb3d93680c430c734a4af93bb7a10a89a4b50d3e3f7542794f83`  
		Last Modified: Tue, 19 Mar 2024 11:23:21 GMT  
		Size: 20.7 MB (20702315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1da3239e5edc67c8b16bcfac0547b3192ca9c72d6ff4c2b70a75c1fc603b92a`  
		Last Modified: Tue, 19 Mar 2024 11:23:20 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a0ef6f4a0295b63760a3bf7374a5a284f8a638ed93daffbd5a45cce75ef8002`  
		Last Modified: Tue, 19 Mar 2024 11:23:20 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8a30a4dc6ad2b3c259aa977fb0c682c830f7378b30ff706598e1cdcaf9f60b`  
		Last Modified: Tue, 19 Mar 2024 11:23:20 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.2-1.1` - unknown; unknown

```console
$ docker pull fluentd@sha256:6bb6c873d1ddaad02174684e6849c64140e7ce2d8c7a265eb7141c8cb14847be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 KB (13622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:147d0ecc047ffef9cf0cd8d4b10a6c0e4476c3e815452f8f4705ab277271275d`

```dockerfile
```

-	Layers:
	-	`sha256:0f24dffc28c7dc5e34e7312399eda20f9fa8901299fe30407fe1e041073dbb17`  
		Last Modified: Tue, 19 Mar 2024 11:23:20 GMT  
		Size: 13.6 KB (13622 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.2-1.1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:9363788cb19d64dcb46eff4b4e5fedfee5bf2e5b040b653ae5930ff27f4e3fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24600146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca741c0cf2897fc408af0ab5f7f500556ae90b9a8293eaeefd60d438c859160d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:c3b6b575eb741f914ec12bd4df43de0cb044a1f2bae7ff15d176e49b5986d903 in / 
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["/bin/sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 20 Sep 2023 09:43:58 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LD_PRELOAD=
# Wed, 20 Sep 2023 09:43:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 Sep 2023 09:43:58 GMT
USER fluent
# Wed, 20 Sep 2023 09:43:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:5385a9a590c3e2872b3ed27554a56fb7ce544c694b41b9b95d70fa86f30b0566`  
		Last Modified: Fri, 26 Jan 2024 23:45:40 GMT  
		Size: 3.3 MB (3258283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91a154538f64991567fc18bd89359c3de3b13651eb79946f1f90b1412e8a6e70`  
		Last Modified: Sat, 16 Mar 2024 17:13:59 GMT  
		Size: 21.3 MB (21339698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9742b74de05dea377e49b47eae37debf6dcfe311b8e8ea9b6ffa75162c074407`  
		Last Modified: Sat, 16 Mar 2024 17:13:58 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553a1c29561145339686a65a76b90eeb345ffe79009291f1fa5b4364956d1643`  
		Last Modified: Sat, 16 Mar 2024 17:13:58 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f161510f8c1addd3cd39b60f67ed679b60dbe064d6629e91b8e6f8a82c0f39f6`  
		Last Modified: Sat, 16 Mar 2024 17:13:58 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.2-1.1` - unknown; unknown

```console
$ docker pull fluentd@sha256:56405b84332edf74042515da848e8660b90d2221105bfc6c83732d51c443d2cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **930.5 KB (930517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4b60dbcdbe9c5fbdbc9c892d33e40d9d7479d5dc2097cff4f79a3019d7a759`

```dockerfile
```

-	Layers:
	-	`sha256:636b6f7ff9b943ce12db4f5d9172f89bce1a857ce9916ea83a53d06fba302d80`  
		Last Modified: Sat, 16 Mar 2024 17:13:58 GMT  
		Size: 916.7 KB (916749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc98a63a414011ab6ef76a74fcc0e91f38597c30113820286b6b17dfe722ef4f`  
		Last Modified: Sat, 16 Mar 2024 17:13:58 GMT  
		Size: 13.8 KB (13768 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.2-1.1` - linux; 386

```console
$ docker pull fluentd@sha256:87556a0eaac45cada6bcd15d537c2c843a6b5d6eaab7ff21349bbe357f925783
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 MB (24395126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:005963481600010f014cf4524e59bf2fe49b147db3517ebe8239b5485c9940c0`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:a7d49c3d7c0292c69f1dade47c5e95e3980c9005bd8cd9ba335627e45e225970 in / 
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["/bin/sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 20 Sep 2023 09:43:58 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LD_PRELOAD=
# Wed, 20 Sep 2023 09:43:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 Sep 2023 09:43:58 GMT
USER fluent
# Wed, 20 Sep 2023 09:43:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:db0c825f4043b16c67d2ecf8030106d2093189b8461779ac49e7c6392a532a13`  
		Last Modified: Sat, 27 Jan 2024 00:39:09 GMT  
		Size: 3.4 MB (3415178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4148a3eac4aaa35790a698ee73a2005a7d4df10da2354cf9fa759c0eb46ca47b`  
		Last Modified: Fri, 15 Mar 2024 23:57:14 GMT  
		Size: 21.0 MB (20977783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd070dc9801a5c9070bc08b77174032a64b0d54af134daa94b6c9334f494ff8a`  
		Last Modified: Fri, 15 Mar 2024 23:57:14 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2057e5a99aa6aeff7497b97ee27d6efbec3c52dfe47cc7af5a9905039df2de28`  
		Last Modified: Fri, 15 Mar 2024 23:57:14 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ebda7b1a05b51cb16303e84d4dd9f7771b388cc305515a945c5fc61428e330`  
		Last Modified: Fri, 15 Mar 2024 23:57:14 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.2-1.1` - unknown; unknown

```console
$ docker pull fluentd@sha256:4d55224a5d81df950c628eb33d0b2d7e6d84709dadeae1ccfe5e15d0b2a13d46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **930.3 KB (930329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f47ab9140c9ee404624c9c1311cbee434e74896a0f571bc9b59687f3ded4e15b`

```dockerfile
```

-	Layers:
	-	`sha256:83d121be6226318aab835208721694e14f21302e43d2a6e84cf20075d1716ef8`  
		Last Modified: Fri, 15 Mar 2024 23:57:14 GMT  
		Size: 916.4 KB (916429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20a3d5c68dad5e3bbd77b7a6397529a93429c91fff02b8207dee39503225153f`  
		Last Modified: Fri, 15 Mar 2024 23:57:14 GMT  
		Size: 13.9 KB (13900 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.2-1.1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:248f70429be97350a580c3dd40affa171909e50df799a34b04c0b4ad1f05057f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 MB (24986237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edf64deb8424068e5b471f8ccb4c4c661163865c6581af1723242b28bada930b`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:142556ae6fb4078ff8df7cd88ef4f1d91b27167561c6e93ceeee4d9a87677a22 in / 
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["/bin/sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 20 Sep 2023 09:43:58 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LD_PRELOAD=
# Wed, 20 Sep 2023 09:43:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 Sep 2023 09:43:58 GMT
USER fluent
# Wed, 20 Sep 2023 09:43:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:c4bf8831607f5d219b98313740266d85a75f3b24c83a4db919b24cc51c6da633`  
		Last Modified: Sat, 27 Jan 2024 00:28:35 GMT  
		Size: 3.4 MB (3392106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03e47551d05f6cb304609791e7d8ad952ccb21b5a6ed83090dea145c7b018ed`  
		Last Modified: Sat, 16 Mar 2024 12:08:22 GMT  
		Size: 21.6 MB (21591953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72de6bde4d31ce7857d9da696bae65f24e0bffcfe80e799c81b3f699ad54d1ae`  
		Last Modified: Sat, 16 Mar 2024 12:08:21 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb79847fa40222fe1af9b58da56f1341e2f5968348cb4de2bd61648f40466cad`  
		Last Modified: Sat, 16 Mar 2024 12:08:21 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880cdf79564ae2ad951b962bc38a099804db192b53ac5a306b85d91085a92dfd`  
		Last Modified: Sat, 16 Mar 2024 12:08:22 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.2-1.1` - unknown; unknown

```console
$ docker pull fluentd@sha256:30a7543e9d7d9ecf7c7501236f8c8ddd79cd95aff5077441f6c0959f40f39e8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **929.0 KB (928998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76046f30be09378029125947bd103ffc56739ca94aca293ecf1679bf77f548d8`

```dockerfile
```

-	Layers:
	-	`sha256:2cd974dba05947f7103ee5683fe11e2c845b46fcbcfb0050d3a29fa14c6f8e28`  
		Last Modified: Sat, 16 Mar 2024 12:08:22 GMT  
		Size: 915.2 KB (915202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a871f6c06d9c14af03812268dd28e70ed1962db7dbbaa1c1bfbdc81fec76ff4e`  
		Last Modified: Sat, 16 Mar 2024 12:08:22 GMT  
		Size: 13.8 KB (13796 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.2-1.1` - linux; s390x

```console
$ docker pull fluentd@sha256:6a0204127ede777d74bea25d0ca72427d2173f4ec04699b87efb14ac002a33c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 MB (24350319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33acaa2070b8b267873becf367d00fb2619763992fad4d7e4afdcf47891483f5`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:332dae9ac04a5dae7353ca7443ee80390b5d93185e9dbde064b470357abc4534 in / 
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["/bin/sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 20 Sep 2023 09:43:58 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LD_PRELOAD=
# Wed, 20 Sep 2023 09:43:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 Sep 2023 09:43:58 GMT
USER fluent
# Wed, 20 Sep 2023 09:43:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:5d54cb3c0670dbeb16e4b7f6005aab36368f0ce33a7cacf5d24d1e62c4618c17`  
		Last Modified: Sat, 27 Jan 2024 00:43:35 GMT  
		Size: 3.2 MB (3176530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd53472e76590c2a8618e674bf6813eadbfafad5b1d0cff6a09ad626b7443db`  
		Last Modified: Sun, 17 Mar 2024 08:52:35 GMT  
		Size: 21.2 MB (21171623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351c9d6d4b6fa9e0747a866e3d4c3e7142b4659bc8438db24b6e288328e99dd2`  
		Last Modified: Sun, 17 Mar 2024 08:52:35 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303f4ceea1ada774bdd6797ffcf69f182bd83761ae22a5699a7e8f3b42bbc35e`  
		Last Modified: Sun, 17 Mar 2024 08:52:35 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85afb89f01c408e989aef554ee040bda1cddebb2aa47827c705ae5a8feecc215`  
		Last Modified: Sun, 17 Mar 2024 08:52:35 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.2-1.1` - unknown; unknown

```console
$ docker pull fluentd@sha256:55d6196eef0ac6d020eb8e2606a7c38b7923d101f535443d91aa29b7df4a1797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **928.5 KB (928519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad92e6306f8d4bedde0e8df286a52d801c631b190f8b8eb2685eb2b4cc95c131`

```dockerfile
```

-	Layers:
	-	`sha256:c9051913d09d39474d3c99c5c8aa10021e9da9f5b9e3e7fad5740d2e1f0a454f`  
		Last Modified: Sun, 17 Mar 2024 08:52:35 GMT  
		Size: 914.6 KB (914592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82ef110b9a4885025231c108e75ef437e47b66812ccfde0dc8e81409bdd9822d`  
		Last Modified: Sun, 17 Mar 2024 08:52:34 GMT  
		Size: 13.9 KB (13927 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16.2-debian-1.1`

```console
$ docker pull fluentd@sha256:533f5df642e8433d5c83c384497136e396d9e8be1c5d2c9b127767de3ee73509
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `fluentd:v1.16.2-debian-1.1` - linux; amd64

```console
$ docker pull fluentd@sha256:7ea25a8471c79337b6ff256d912d5593773fb5735e974c4d92fb283a8f6e3ac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101283905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c2e4c91448fb59e27d9d889166c38410db0ab5d709ea6350e028f8ff1e933b`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:43:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LANG=C.UTF-8
# Wed, 20 Sep 2023 09:43:58 GMT
ENV RUBY_VERSION=3.1.6
# Wed, 20 Sep 2023 09:43:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.1/ruby-3.1.6.tar.xz
# Wed, 20 Sep 2023 09:43:58 GMT
ENV RUBY_DOWNLOAD_SHA256=597bd1849f252d8a6863cb5d38014ac54152b508c36dca156f6356a9e63c6102
# Wed, 20 Sep 2023 09:43:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 Sep 2023 09:43:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 Sep 2023 09:43:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 09:43:58 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["irb"]
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 20 Sep 2023 09:43:58 GMT
ENV TINI_VERSION=0.18.0
# Wed, 20 Sep 2023 09:43:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 20 Sep 2023 09:43:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 Sep 2023 09:43:58 GMT
USER fluent
# Wed, 20 Sep 2023 09:43:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9082bd5a89037e709a10a4a21acfee0b84fd88a794d8e4fb0c10176f2b8293a`  
		Last Modified: Wed, 29 May 2024 23:03:55 GMT  
		Size: 9.8 MB (9815742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea461a053a2dbc652fe71eeed34571bdf8c953184ec6f1a706fe394b640615e`  
		Last Modified: Wed, 29 May 2024 23:03:54 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ab168a37ec4dfdb009b9f749b96df7fa4c3cb46aae1b60425ff80437b19e23`  
		Last Modified: Wed, 29 May 2024 23:03:55 GMT  
		Size: 32.5 MB (32467562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519e60aa436396ec421b4659295c2bf4b68d2ddce63acd84652cc579599102bc`  
		Last Modified: Wed, 29 May 2024 23:03:54 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530c9b07e5e9993f79b2adaef2281822c862b6effc8cda9df38f36390015aa7c`  
		Last Modified: Wed, 29 May 2024 23:59:12 GMT  
		Size: 27.6 MB (27563736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b9e0dcf1e7e6e633efee3014532c5a54bcd5b118f8fd0e34b1175c3e635c897`  
		Last Modified: Wed, 29 May 2024 23:59:12 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3dd8469604ccd79f343655da0ad1c374250be62e5bcc5a0d4d2ca841c62029`  
		Last Modified: Wed, 29 May 2024 23:59:12 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c142c6ff8dc368ba27db532b08ebf042e2b1a1be48f6fe434230e3e31fd373b`  
		Last Modified: Wed, 29 May 2024 23:59:12 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.2-debian-1.1` - unknown; unknown

```console
$ docker pull fluentd@sha256:745e9d3f36857caefe0a67d7308367395ddd5a5db2738750c63e913bab53127d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4121510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35260245b6107885d52a2f50236b0971025ca4a2f39ae946697608193641ab58`

```dockerfile
```

-	Layers:
	-	`sha256:9e2dc15e9046fbd9008c1557162ce3f835c1629f170ad9ef8438439132c9285d`  
		Last Modified: Wed, 29 May 2024 23:59:12 GMT  
		Size: 4.1 MB (4100445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a23bf22989b2fdff2264c8d0c57ca277d96b4c02f38425354ffd93f0b134c1ed`  
		Last Modified: Wed, 29 May 2024 23:59:12 GMT  
		Size: 21.1 KB (21065 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.2-debian-1.1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:fc92ea3152b0c8fe2700ad4163072613688143b2f7f84ef280f1f9b489bad004
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94804559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de59fba9727de3ece8a43a69ae8667d2b0c0c338657e9a230ece022ee052c48`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:7a63cf2b5d16adf102fbd2452be219224667c4ea55981247f398a4a867ef96c4 in / 
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:43:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LANG=C.UTF-8
# Wed, 20 Sep 2023 09:43:58 GMT
ENV RUBY_VERSION=3.1.6
# Wed, 20 Sep 2023 09:43:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.1/ruby-3.1.6.tar.xz
# Wed, 20 Sep 2023 09:43:58 GMT
ENV RUBY_DOWNLOAD_SHA256=597bd1849f252d8a6863cb5d38014ac54152b508c36dca156f6356a9e63c6102
# Wed, 20 Sep 2023 09:43:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 Sep 2023 09:43:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 Sep 2023 09:43:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 09:43:58 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["irb"]
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 20 Sep 2023 09:43:58 GMT
ENV TINI_VERSION=0.18.0
# Wed, 20 Sep 2023 09:43:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 20 Sep 2023 09:43:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 Sep 2023 09:43:58 GMT
USER fluent
# Wed, 20 Sep 2023 09:43:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:b6ea79e472ea80a508a2732ddeb0e19de51d3f0aaf8f0fd18c1cdd1c939d49de`  
		Last Modified: Tue, 14 May 2024 00:52:17 GMT  
		Size: 28.9 MB (28936721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33cbc8081ab7d7b6be84a5e608e5fd1f98691dd8a1cd02b9a291eedf4964a17d`  
		Last Modified: Wed, 29 May 2024 23:24:24 GMT  
		Size: 8.4 MB (8429217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83ddd53ec367faf472712ad792c2f294c042f57bc066e861839ccbe5b6f1069`  
		Last Modified: Wed, 29 May 2024 23:24:23 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e80bc0b2c35753df606135c4129ed1828702ca3d91ce760ab84a7ab6212307a`  
		Last Modified: Wed, 29 May 2024 23:24:25 GMT  
		Size: 31.0 MB (31016093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a57b966212874b49581cb4e64e211df8356706b7847fb5f35789626f0982d7c`  
		Last Modified: Wed, 29 May 2024 23:24:24 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66307f145e38aa0d8a4a40f17bd604c3077e1d4bfe8d1ea88ae111e99038fa96`  
		Last Modified: Thu, 30 May 2024 00:05:23 GMT  
		Size: 26.4 MB (26419604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e4661a5bb357fe29b6b84fcfba22d8c0ea435f32aefbcf073c1c1c95a147d9`  
		Last Modified: Thu, 30 May 2024 00:05:22 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1939d0b5f05f84aad8d87f37400706f43132c07623da6e23b918ba5d30be05`  
		Last Modified: Thu, 30 May 2024 00:05:22 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e7130f8cfbe0d908ad46ceec6671fb80b774d9a5971e79f38da8b329ce3322`  
		Last Modified: Thu, 30 May 2024 00:05:22 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.2-debian-1.1` - unknown; unknown

```console
$ docker pull fluentd@sha256:3f913bf0d3fb424edcae62a693306f12f6d1b2c12d782acf859d6c241d61a58f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4092828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ac8fee0c7d21191abda77720592137a7a11075246566d7b4fc9a1b58f443160`

```dockerfile
```

-	Layers:
	-	`sha256:fbd4eae738d470dc66f79d324816fd72ce57797f140e0bd3f09a4cf5fb1b3db4`  
		Last Modified: Thu, 30 May 2024 00:05:22 GMT  
		Size: 4.1 MB (4071659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c99f70914906ca3563346406ff52069f9b06b239fbd56836ab8a0e18ec8554a9`  
		Last Modified: Thu, 30 May 2024 00:05:22 GMT  
		Size: 21.2 KB (21169 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.2-debian-1.1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:f56e1e20f567e9455829b20c8e342a9cc07ca2dce6ba6dc22b4a6d6ce83b78e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.7 MB (91683933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:989a1123ac3fc7ef3c543316517ebc4bfc6227e9b4cea83b0b7edc4d113d178b`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:b58f353e9d2a24c2c16ae0913b28705d3ecc439d60d82b5b4982780c59aae249 in / 
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:43:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LANG=C.UTF-8
# Wed, 20 Sep 2023 09:43:58 GMT
ENV RUBY_VERSION=3.1.5
# Wed, 20 Sep 2023 09:43:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.1/ruby-3.1.5.tar.xz
# Wed, 20 Sep 2023 09:43:58 GMT
ENV RUBY_DOWNLOAD_SHA256=f9375a45bdf1cc41298558e7ac6c367f7b6cdcccf7196618b21f0886ff583b91
# Wed, 20 Sep 2023 09:43:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 Sep 2023 09:43:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 Sep 2023 09:43:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 09:43:58 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["irb"]
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 20 Sep 2023 09:43:58 GMT
ENV TINI_VERSION=0.18.0
# Wed, 20 Sep 2023 09:43:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 20 Sep 2023 09:43:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 Sep 2023 09:43:58 GMT
USER fluent
# Wed, 20 Sep 2023 09:43:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:a5c0b9604ae49509a7875b258d98493d63bdb4c1c27a70f2befa5fa4fcea1888`  
		Last Modified: Tue, 14 May 2024 01:13:30 GMT  
		Size: 26.6 MB (26594493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b2ac23e89df319720e3958b1f2d3a5fc86dfef34df01d524fc76564f5ec6858`  
		Last Modified: Tue, 14 May 2024 19:54:15 GMT  
		Size: 7.9 MB (7937129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5f1ded0e7e04ee269a1a441a15e3dcb25dec72c008121e727785185949be7f`  
		Last Modified: Tue, 14 May 2024 19:54:14 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8711b18a55f2058f9d4cf5f5145f1c65d307c48bb185356d36ab3d5df1da0578`  
		Last Modified: Tue, 14 May 2024 20:16:20 GMT  
		Size: 30.9 MB (30890606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa25f54f1918243acee6f251f389b3dceb9abf85e2c3e1e822a40742d7dd6dd`  
		Last Modified: Tue, 14 May 2024 20:16:19 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f2d15a225d8cddfa78b7ba48f475407fa3fd0ca4be7416862f4f063f0fabcd`  
		Last Modified: Wed, 15 May 2024 08:48:30 GMT  
		Size: 26.3 MB (26258784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da985258c02a7ceda7071a85fab755a831eff9097ec8dc50ab880767559c839`  
		Last Modified: Wed, 15 May 2024 08:48:29 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd1f641446a73af8575096e6b16d56f890d2b24796ce5f1b7c5b5fbc6533d62`  
		Last Modified: Wed, 15 May 2024 08:48:29 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb444b5572b53637ebb6c19d4acb946896f6d55730cb546e51f2c66aa45cf190`  
		Last Modified: Wed, 15 May 2024 08:48:29 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.2-debian-1.1` - unknown; unknown

```console
$ docker pull fluentd@sha256:618d6585f4428904935200b2afd774f2b54ed76b046a53af9192c86788a11ac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4096388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db669692a0e590e2bd9611d1b5400cce9fde931a8c842db2a05c5816b51dcd5f`

```dockerfile
```

-	Layers:
	-	`sha256:13af4ba4fa920ee05c40fabdcc002d70a359003f6a7b5f98ffc3ad26cda1f3d4`  
		Last Modified: Wed, 15 May 2024 08:48:29 GMT  
		Size: 4.1 MB (4074427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce265ce0c76a07f84c415d02c91c1998ddb9010445065d6dedf7c10924999f79`  
		Last Modified: Wed, 15 May 2024 08:48:29 GMT  
		Size: 22.0 KB (21961 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.2-debian-1.1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:b37b9baf78fd96ede20a219c158bb85cc70d1b9f573b2e95647f27d57537e2a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.3 MB (98312576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df277e7e81c2504353635abb1a797cde7355cf7be21b875a227b60bf8c99b2c6`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:43:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LANG=C.UTF-8
# Wed, 20 Sep 2023 09:43:58 GMT
ENV RUBY_VERSION=3.1.5
# Wed, 20 Sep 2023 09:43:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.1/ruby-3.1.5.tar.xz
# Wed, 20 Sep 2023 09:43:58 GMT
ENV RUBY_DOWNLOAD_SHA256=f9375a45bdf1cc41298558e7ac6c367f7b6cdcccf7196618b21f0886ff583b91
# Wed, 20 Sep 2023 09:43:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 Sep 2023 09:43:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 Sep 2023 09:43:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 09:43:58 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["irb"]
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 20 Sep 2023 09:43:58 GMT
ENV TINI_VERSION=0.18.0
# Wed, 20 Sep 2023 09:43:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 20 Sep 2023 09:43:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 Sep 2023 09:43:58 GMT
USER fluent
# Wed, 20 Sep 2023 09:43:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a0d9118b4abd2d5feec7b459ee3bdca44f2aef03dc342fad499ad497af4c47`  
		Last Modified: Tue, 14 May 2024 22:36:20 GMT  
		Size: 9.0 MB (9036885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da555d0f96d5a45244d417af80eeb351678c49220acfa3080a31e1d53de6fcff`  
		Last Modified: Tue, 14 May 2024 22:36:20 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488f4b09e69ab09fe12d719b25b254d37cc5c19d86ddd3383f4ff9993c15fdde`  
		Last Modified: Tue, 14 May 2024 23:35:25 GMT  
		Size: 31.8 MB (31836703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8441e3698a1ec01cede57326ce007515dd33a7b1c5ed94e9eadaa420ebf8adcb`  
		Last Modified: Tue, 14 May 2024 23:35:25 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d5fa3e7aeca62fa74dcc5af65f95cbe381a5e56b2c8aa94f29529434114224`  
		Last Modified: Wed, 15 May 2024 16:28:46 GMT  
		Size: 27.3 MB (27349151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d17cf858e4773259edc64bfa39ac59390ff0bf908e023cbef9e1baa3503421b`  
		Last Modified: Wed, 15 May 2024 16:28:45 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5cf6a208196cc026d25c432def3f865bca0488bc885d44e1b13edaa0483b6b`  
		Last Modified: Wed, 15 May 2024 16:28:45 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60e8d03118d1489980e302a46f27564c3e2f0aa53770bcf523605ae4855983c`  
		Last Modified: Wed, 15 May 2024 16:28:45 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.2-debian-1.1` - unknown; unknown

```console
$ docker pull fluentd@sha256:1faadb74443cb8d29fb2547ae3390e9bc3b1416bcae81306162ec78d074986ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4096681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add83f8a4d18b1be46149e7c8067bac31d08727b4b50fa3fb714baabbf293f54`

```dockerfile
```

-	Layers:
	-	`sha256:9499bcf28a0d3b20b89ebc0968b72f58299db84b84668757f30736995a27c0bc`  
		Last Modified: Wed, 15 May 2024 16:28:46 GMT  
		Size: 4.1 MB (4074782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b6a37df529f05a1a674708d72330c4f5f793f3f167a1dc5b1a3999d0cf9ba7b`  
		Last Modified: Wed, 15 May 2024 16:28:45 GMT  
		Size: 21.9 KB (21899 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.2-debian-1.1` - linux; 386

```console
$ docker pull fluentd@sha256:2cd66687f3140602933bed40a9549c69830191664af9ce34029bafbadf704a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101698588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:855c64704bb29070d11f3939e973a3ff262a6e06b67b2855ec9f8a4e49c6adf4`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:8cc17bd8431911317f7d91df00ff305ed2f31f83f3224da64f6d7b9c38819dae in / 
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:43:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LANG=C.UTF-8
# Wed, 20 Sep 2023 09:43:58 GMT
ENV RUBY_VERSION=3.1.6
# Wed, 20 Sep 2023 09:43:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.1/ruby-3.1.6.tar.xz
# Wed, 20 Sep 2023 09:43:58 GMT
ENV RUBY_DOWNLOAD_SHA256=597bd1849f252d8a6863cb5d38014ac54152b508c36dca156f6356a9e63c6102
# Wed, 20 Sep 2023 09:43:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 Sep 2023 09:43:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 Sep 2023 09:43:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 09:43:58 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["irb"]
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 20 Sep 2023 09:43:58 GMT
ENV TINI_VERSION=0.18.0
# Wed, 20 Sep 2023 09:43:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 20 Sep 2023 09:43:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 Sep 2023 09:43:58 GMT
USER fluent
# Wed, 20 Sep 2023 09:43:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:de7432ff839295b583814dfc21a6afb18eb4e45d8144c26b1402229e5bc8105f`  
		Last Modified: Tue, 14 May 2024 00:52:45 GMT  
		Size: 32.4 MB (32424043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3a568a45828b1d1298f4d99959795046d53abb6d4d63888199208cbf741172`  
		Last Modified: Wed, 29 May 2024 23:03:58 GMT  
		Size: 11.8 MB (11791241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e97e3dd3c171d5e9fec973c4ead6b2c692d2770a7857701b085270a61f4db0`  
		Last Modified: Wed, 29 May 2024 23:03:57 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d04aed719335219282911ec2a861542ed0c99ec89013f0cc2adb69d9959696`  
		Last Modified: Wed, 29 May 2024 23:03:59 GMT  
		Size: 31.0 MB (31034408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d972742b85775ff020962d4ddc3864adee1aaf742f00c1270bef40cacfeff65`  
		Last Modified: Wed, 29 May 2024 23:03:58 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:517efb1e5ca0c4698725df3d8d41156d9185428768294a137e6ae0cfaf468348`  
		Last Modified: Wed, 29 May 2024 23:59:06 GMT  
		Size: 26.4 MB (26445972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6780445ce7f3d5c77287f446bd3a8dfbd303a36a553a6e4b2e711de394376d`  
		Last Modified: Wed, 29 May 2024 23:59:06 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6469bde1f30d98a5801181e01f1e520f9d859660e00b04ed88ab871f1bfeaaa8`  
		Last Modified: Wed, 29 May 2024 23:59:06 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a573623fb52af81da685c6d1f0c9a5ee58948bb96fe2d608292ee5dc21ee34db`  
		Last Modified: Wed, 29 May 2024 23:59:06 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.2-debian-1.1` - unknown; unknown

```console
$ docker pull fluentd@sha256:58f226a999c131152fcb6bf46313384a81117f574c2acc682fbfbe9f9dc1290f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4125699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ac51640d97fc07d4ec6d6a6a2b72e68fbdbc1c3f978f7ccc61036d99dfeb929`

```dockerfile
```

-	Layers:
	-	`sha256:a65136730f98ae64b27e2f1cd4a89958d34c14ab6132032f1bdbbc8be71d9880`  
		Last Modified: Wed, 29 May 2024 23:59:06 GMT  
		Size: 4.1 MB (4104652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63498123fe8b580ddeaf93d6a2318404badc699a70f4424aa72f5f184097f30b`  
		Last Modified: Wed, 29 May 2024 23:59:06 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.2-debian-1.1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:c58d402cd73a61a8719055d598c3d34030b35d5c459cbb4172aa6a18e242528d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106317383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4c86c71f1ddbeaeb57fb181709d57677a6d08399c9993b872245bbe64357ec`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:7c74907a13931bf5f38ce8642536ee05738ba9d233424998c52fc548130034b5 in / 
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:43:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LANG=C.UTF-8
# Wed, 20 Sep 2023 09:43:58 GMT
ENV RUBY_VERSION=3.1.5
# Wed, 20 Sep 2023 09:43:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.1/ruby-3.1.5.tar.xz
# Wed, 20 Sep 2023 09:43:58 GMT
ENV RUBY_DOWNLOAD_SHA256=f9375a45bdf1cc41298558e7ac6c367f7b6cdcccf7196618b21f0886ff583b91
# Wed, 20 Sep 2023 09:43:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 Sep 2023 09:43:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 Sep 2023 09:43:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 09:43:58 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["irb"]
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 20 Sep 2023 09:43:58 GMT
ENV TINI_VERSION=0.18.0
# Wed, 20 Sep 2023 09:43:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 20 Sep 2023 09:43:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 Sep 2023 09:43:58 GMT
USER fluent
# Wed, 20 Sep 2023 09:43:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:8fd45f8fa7e828bdb5dd8878febd6f367c5092a047db5f6ca094056a1b0c627c`  
		Last Modified: Tue, 14 May 2024 01:24:52 GMT  
		Size: 35.3 MB (35311159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77eaf038fe95ed309a54977b60e55f1d616cfb95ff9b10e60f7cae3eb1170ca6`  
		Last Modified: Tue, 14 May 2024 16:21:18 GMT  
		Size: 10.3 MB (10276044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0dd0072d29e123334a97df766bd98dbdbcae449a8731c89e8068d669ab561f1`  
		Last Modified: Tue, 14 May 2024 16:21:17 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d558d400b4bcf627df89f26db603f01271c88447c4cd8b8aa65f63e18e97f2`  
		Last Modified: Tue, 14 May 2024 16:35:01 GMT  
		Size: 32.7 MB (32650680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb545335c09afd49c5ab46011643532b1432001efebfc2ee1c23e9aa85b9247b`  
		Last Modified: Tue, 14 May 2024 16:35:00 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b1723c886e41a8430ac12a3ee7b7dc1e8aaf241ffaf4347f7fee5e123b38bb`  
		Last Modified: Wed, 15 May 2024 05:29:06 GMT  
		Size: 28.1 MB (28076573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6469099fe3687b027cbe49a9b54caa0298de7f35ce1969c3cc7e0cd8ab0a8b3a`  
		Last Modified: Wed, 15 May 2024 05:29:05 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19956713298118dda41b05a3ec0f484ae0c9af4f0cc30d13f3d7b09bfa72a01`  
		Last Modified: Wed, 15 May 2024 05:29:06 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e77bc938f620a386632604696f4d850114e087163e0f06e892af60a48b5e66`  
		Last Modified: Wed, 15 May 2024 05:29:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.2-debian-1.1` - unknown; unknown

```console
$ docker pull fluentd@sha256:25382af1f11d10de3b6aee6c3b36b58ad4960e2cf4f22f52e52c8617ed6e8c04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4111265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab12ea329458719a2a852b6ba98b6ddc5d90a17a6bc42b48de6ebd2b8ac5b2d`

```dockerfile
```

-	Layers:
	-	`sha256:0cead822999fda491b4c61bf54687df43deea1772278411200bbc99f97ffafd1`  
		Last Modified: Wed, 15 May 2024 05:29:05 GMT  
		Size: 4.1 MB (4089337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0aa7c95f63163520218f9067b676d23f4bfc7883428b5ef0e89a3cae83ab832b`  
		Last Modified: Wed, 15 May 2024 05:29:05 GMT  
		Size: 21.9 KB (21928 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.2-debian-1.1` - linux; s390x

```console
$ docker pull fluentd@sha256:1120657de1a63464e03ff4a193e3ca9e45762eb54e15b1291ddda9bbdc7fbd6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98443866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f15088fd1c4701a9428f92106d3e4629e5daf2f63e338ca9425afacac84c83b`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 20 Sep 2023 09:43:58 GMT
ADD file:bac230200161ff0b0332af3dc90dc1aba6bdeb875d95659699251b2af4eec8dc in / 
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:43:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LANG=C.UTF-8
# Wed, 20 Sep 2023 09:43:58 GMT
ENV RUBY_VERSION=3.1.5
# Wed, 20 Sep 2023 09:43:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.1/ruby-3.1.5.tar.xz
# Wed, 20 Sep 2023 09:43:58 GMT
ENV RUBY_DOWNLOAD_SHA256=f9375a45bdf1cc41298558e7ac6c367f7b6cdcccf7196618b21f0886ff583b91
# Wed, 20 Sep 2023 09:43:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 Sep 2023 09:43:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 Sep 2023 09:43:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 09:43:58 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["irb"]
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 Sep 2023 09:43:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.2
# Wed, 20 Sep 2023 09:43:58 GMT
ENV TINI_VERSION=0.18.0
# Wed, 20 Sep 2023 09:43:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.2.6  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2 && gem install uri -v 0.12.2  && gem install fluentd -v 1.16.2  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 Sep 2023 09:43:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 Sep 2023 09:43:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 20 Sep 2023 09:43:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 Sep 2023 09:43:58 GMT
USER fluent
# Wed, 20 Sep 2023 09:43:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 Sep 2023 09:43:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:14d39445de105c0a8fe00b3899e9fdab7cdfbb3ff27c8b39dd9059f3264a4841`  
		Last Modified: Tue, 14 May 2024 00:48:06 GMT  
		Size: 29.7 MB (29673656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c3fa34390dfcb4371e42b7087cc2aea1a4f78c53b90bd2236df2ac51939fcca`  
		Last Modified: Tue, 14 May 2024 23:49:14 GMT  
		Size: 8.7 MB (8656969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d975f167082b1dee6574bbada3e46d74a2ccc11f8ca7335acb5d1176e278d09a`  
		Last Modified: Tue, 14 May 2024 23:49:13 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115fde46bf9e7631e29084b296c364a52437a3a8bf81d484fb6cbed589b29f35`  
		Last Modified: Wed, 15 May 2024 00:35:30 GMT  
		Size: 32.3 MB (32299053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0ced180afb5290ebfd1648aac980679b1a5233a6d382b39688db22b84361f9`  
		Last Modified: Wed, 15 May 2024 00:35:29 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d3f5d684ec1600fafdfea3bff643c9f583db014632b3c8744a3b168b9fa6c0`  
		Last Modified: Wed, 15 May 2024 03:31:10 GMT  
		Size: 27.8 MB (27811255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ad37f60f7dad780a79d16a0790eebc7aea4f92eefd5431d37a9694fcfeac74`  
		Last Modified: Wed, 15 May 2024 03:31:09 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629fc2797ec37760927f9cf727dcb4ddef081eaa280360db13ab61faf62c8967`  
		Last Modified: Wed, 15 May 2024 03:31:09 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9367bec0ed2db3b7bd4618f3ebc5f6c8fa712eb72b835d25e484809a295cf0ac`  
		Last Modified: Wed, 15 May 2024 03:31:09 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.2-debian-1.1` - unknown; unknown

```console
$ docker pull fluentd@sha256:596c553520817882fc5ff58151c9020786097af4de2d7275c2a487b4a71e7563
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4111010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ea34d975544f1d6b509290a59ee569f844eaf05f255820939b18e90c3c88b2`

```dockerfile
```

-	Layers:
	-	`sha256:bb14a10da8944e5f08710cfd825833929f0cbc8923324a6dc079f9f27ba03854`  
		Last Modified: Wed, 15 May 2024 03:31:09 GMT  
		Size: 4.1 MB (4089122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee61cbec8ff5df433bbe16c4c3374481e1d2ba39b88aa83c60a250dc7ef8b318`  
		Last Modified: Wed, 15 May 2024 03:31:09 GMT  
		Size: 21.9 KB (21888 bytes)  
		MIME: application/vnd.in-toto+json
