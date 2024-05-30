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
$ docker pull fluentd@sha256:7bff91843b3f4eb50accdd1007328e2e0ac8435b7f1941821f3ce82ce8a69a5c
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
$ docker pull fluentd@sha256:42760096c8113eaa55665b2791748dd3e4f5847c958479727b5ab3a7f6533b87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.7 MB (91686053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ffb17d6cdb8278b08ff209c82d058445730883caf201eaa1188ea1def86ef0f`
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
	-	`sha256:a5c0b9604ae49509a7875b258d98493d63bdb4c1c27a70f2befa5fa4fcea1888`  
		Last Modified: Tue, 14 May 2024 01:13:30 GMT  
		Size: 26.6 MB (26594493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d918ba3b35ac5f944312ef73b514e2d51e7f4e66754dff934c420663a3865a`  
		Last Modified: Thu, 30 May 2024 03:46:31 GMT  
		Size: 7.9 MB (7937155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f706c94cfb85451a5f43141e14f56e1afbd638a49072e934a558a7cb8c6673ec`  
		Last Modified: Thu, 30 May 2024 03:46:31 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5cddb82ca49108ac9d389a2362f5244c6988e5eb96dddebfe539947ecbd831`  
		Last Modified: Thu, 30 May 2024 03:46:32 GMT  
		Size: 30.9 MB (30890835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52c183e312386df687ae4bc8ce00f063391d60294b3894b256f75f39941ebbd`  
		Last Modified: Thu, 30 May 2024 03:46:31 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aef7e43f94ecb9f9e8cb3599d6dc6be029da8070ed77084e93783fdb75c2e0c`  
		Last Modified: Thu, 30 May 2024 04:38:27 GMT  
		Size: 26.3 MB (26260635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb558102bb8e4205aa2a26dfdd8beeed53d087979a9ba4685074e3d13a65083`  
		Last Modified: Thu, 30 May 2024 04:38:26 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714262418e68ff28023d716ab427ac3d17c8e1e6000bcbb0dfecb57f72263d0c`  
		Last Modified: Thu, 30 May 2024 04:38:26 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3db548dcbe60ff071fba9c71a94b3af7646f7bcc9dde760eca54820079b665b`  
		Last Modified: Thu, 30 May 2024 04:38:26 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:47902a5f7b3411b3674930f3fb1e850b9c169b53bb07f7eab2899c28f7ae8b03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4095596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98be3a5719745f70b224cf0f51146797255926a9abea754e4d7def7deb43fce`

```dockerfile
```

-	Layers:
	-	`sha256:791f6b2ee898779a2299d0550b78de98b268fc1bb33cc342192e7976096da83a`  
		Last Modified: Thu, 30 May 2024 04:38:26 GMT  
		Size: 4.1 MB (4074427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:515e062edca226937692580ef75add6925d62972ae37c41a67447f772a5e62dd`  
		Last Modified: Thu, 30 May 2024 04:38:25 GMT  
		Size: 21.2 KB (21169 bytes)  
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
$ docker pull fluentd@sha256:db3b84e1fb7f8ff619870e2eb87bf4e09295f3f771bc03c062df5949593d24e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106326565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:152b9384fc036cd1ec19c2b67e721ed283d158974251768dcbf58594e8e8e6a9`
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
	-	`sha256:8fd45f8fa7e828bdb5dd8878febd6f367c5092a047db5f6ca094056a1b0c627c`  
		Last Modified: Tue, 14 May 2024 01:24:52 GMT  
		Size: 35.3 MB (35311159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550b27601761a991b3de6e3a4b4e4d50fe6c7ffb31541865520b721cf3746177`  
		Last Modified: Thu, 30 May 2024 03:31:39 GMT  
		Size: 10.3 MB (10276045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c43d86ea69e721acb85f2599759aad0235a69f04a8d7f091a8be4447cba69c4d`  
		Last Modified: Thu, 30 May 2024 03:31:38 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4295834ee6788da085a04107d75cfc88aa66d02f54a1609901cf700be52c48`  
		Last Modified: Thu, 30 May 2024 03:31:43 GMT  
		Size: 32.6 MB (32649905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae11a948e3f0a888ac5e43d357f5a1b0b133be7108e884a68ff43c0b34c0e16`  
		Last Modified: Thu, 30 May 2024 03:31:38 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b73edd05fab5804ef5fa4f8f68f8032bd4f05dfe31f51dad187693b1d1ce324`  
		Last Modified: Thu, 30 May 2024 05:43:36 GMT  
		Size: 28.1 MB (28086522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38b2452960347b3813b6d5f441f05e5f56a7352af83c312237789d581d9c032`  
		Last Modified: Thu, 30 May 2024 05:43:35 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26efb4e0780a37e1b383e1a9a1282701ab9b1ffad52816d5efbde60074a2d601`  
		Last Modified: Thu, 30 May 2024 05:43:35 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dcdd780a4719cce4e8d0fb8fc6951f871efef09fb2a0af8d1e4df3d0ccc77ef`  
		Last Modified: Thu, 30 May 2024 05:43:35 GMT  
		Size: 461.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:12a3829a82e0ad07b4dc862cd64f198ea61710c8edfae92bcea7da28fd0e521c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4110471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d09596edf8142ea948203497f3b17cb65b28f2f246e2d57b98a1755bd7d1d0d`

```dockerfile
```

-	Layers:
	-	`sha256:517e07661428aa4f3149761c9fa80768b88448239b6a3ebb8b7847932535ea01`  
		Last Modified: Thu, 30 May 2024 05:43:35 GMT  
		Size: 4.1 MB (4089337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fd6d73da6f077ad50dc48a66f54224a30c4643b0723c88b3397829a3084c68f`  
		Last Modified: Thu, 30 May 2024 05:43:35 GMT  
		Size: 21.1 KB (21134 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; s390x

```console
$ docker pull fluentd@sha256:63c1e2d1778cc7d0d84bcbe5dd4413d7e2f8456bf45620473193fbac468449e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98447641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beeebab531289ee35b3a37c37b154440d6c884a5288827feedf2b5b2b6b26aeb`
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
	-	`sha256:14d39445de105c0a8fe00b3899e9fdab7cdfbb3ff27c8b39dd9059f3264a4841`  
		Last Modified: Tue, 14 May 2024 00:48:06 GMT  
		Size: 29.7 MB (29673656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b73b2f4b8a0b336038e774c205e2deaa818f1f9e22bd62b45a8061e0b45008`  
		Last Modified: Thu, 30 May 2024 01:45:07 GMT  
		Size: 8.7 MB (8656975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1a3cca988af307896aeee64218238ef66b6044f4b680960e969a3a7b5572d6`  
		Last Modified: Thu, 30 May 2024 01:45:05 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:660ab6701a0469203cf24e6e0a39e2e6c41af532d2e13e67c00b0dd1d6b8c97c`  
		Last Modified: Thu, 30 May 2024 01:45:06 GMT  
		Size: 32.3 MB (32300418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d1d3a9417752e15732b1aed70f9cdb71862503c260fb1a47ee5434352a53807`  
		Last Modified: Thu, 30 May 2024 01:45:05 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff48d398f8d63ed56755a1f257a4084f9ad307b57112023b4cfd15b46abebd2`  
		Last Modified: Thu, 30 May 2024 03:17:32 GMT  
		Size: 27.8 MB (27813664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d0a537cc9fec20d2ffcb7ea92b9e206a6fa820b8531464863634a95494456d`  
		Last Modified: Thu, 30 May 2024 03:17:31 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1838409b967ce4d3c54b498a212615d5a4cfbab564fcc5c65f10a8ad3ece1705`  
		Last Modified: Thu, 30 May 2024 03:17:31 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0599901586b51a0c7db0f36a1288ff7b59e0d353d9b8cd6f2c30b35d74a9166`  
		Last Modified: Thu, 30 May 2024 03:17:32 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:cf9a594bac147f2d091673e7b22b7b5231f4a83613c0549a2cb92ed1309dc0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4110218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06900592d43cbee03f32ea8ebbac857a5ce24ebb5ad79606396a1b2f7a9ce2b6`

```dockerfile
```

-	Layers:
	-	`sha256:6c34a61d9a7b51d53007fdd392bd3be70b38de01f48158a5b79c01f8b1afa15d`  
		Last Modified: Thu, 30 May 2024 03:17:31 GMT  
		Size: 4.1 MB (4089122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86a620abeb8d1949228f0dd330ed89f2586fe3e116f18a718ebfd33a488dbe98`  
		Last Modified: Thu, 30 May 2024 03:17:31 GMT  
		Size: 21.1 KB (21096 bytes)  
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
$ docker pull fluentd@sha256:7bff91843b3f4eb50accdd1007328e2e0ac8435b7f1941821f3ce82ce8a69a5c
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
$ docker pull fluentd@sha256:42760096c8113eaa55665b2791748dd3e4f5847c958479727b5ab3a7f6533b87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.7 MB (91686053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ffb17d6cdb8278b08ff209c82d058445730883caf201eaa1188ea1def86ef0f`
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
	-	`sha256:a5c0b9604ae49509a7875b258d98493d63bdb4c1c27a70f2befa5fa4fcea1888`  
		Last Modified: Tue, 14 May 2024 01:13:30 GMT  
		Size: 26.6 MB (26594493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d918ba3b35ac5f944312ef73b514e2d51e7f4e66754dff934c420663a3865a`  
		Last Modified: Thu, 30 May 2024 03:46:31 GMT  
		Size: 7.9 MB (7937155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f706c94cfb85451a5f43141e14f56e1afbd638a49072e934a558a7cb8c6673ec`  
		Last Modified: Thu, 30 May 2024 03:46:31 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5cddb82ca49108ac9d389a2362f5244c6988e5eb96dddebfe539947ecbd831`  
		Last Modified: Thu, 30 May 2024 03:46:32 GMT  
		Size: 30.9 MB (30890835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52c183e312386df687ae4bc8ce00f063391d60294b3894b256f75f39941ebbd`  
		Last Modified: Thu, 30 May 2024 03:46:31 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aef7e43f94ecb9f9e8cb3599d6dc6be029da8070ed77084e93783fdb75c2e0c`  
		Last Modified: Thu, 30 May 2024 04:38:27 GMT  
		Size: 26.3 MB (26260635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb558102bb8e4205aa2a26dfdd8beeed53d087979a9ba4685074e3d13a65083`  
		Last Modified: Thu, 30 May 2024 04:38:26 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714262418e68ff28023d716ab427ac3d17c8e1e6000bcbb0dfecb57f72263d0c`  
		Last Modified: Thu, 30 May 2024 04:38:26 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3db548dcbe60ff071fba9c71a94b3af7646f7bcc9dde760eca54820079b665b`  
		Last Modified: Thu, 30 May 2024 04:38:26 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.2-debian-1.1` - unknown; unknown

```console
$ docker pull fluentd@sha256:47902a5f7b3411b3674930f3fb1e850b9c169b53bb07f7eab2899c28f7ae8b03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4095596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98be3a5719745f70b224cf0f51146797255926a9abea754e4d7def7deb43fce`

```dockerfile
```

-	Layers:
	-	`sha256:791f6b2ee898779a2299d0550b78de98b268fc1bb33cc342192e7976096da83a`  
		Last Modified: Thu, 30 May 2024 04:38:26 GMT  
		Size: 4.1 MB (4074427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:515e062edca226937692580ef75add6925d62972ae37c41a67447f772a5e62dd`  
		Last Modified: Thu, 30 May 2024 04:38:25 GMT  
		Size: 21.2 KB (21169 bytes)  
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
$ docker pull fluentd@sha256:db3b84e1fb7f8ff619870e2eb87bf4e09295f3f771bc03c062df5949593d24e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106326565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:152b9384fc036cd1ec19c2b67e721ed283d158974251768dcbf58594e8e8e6a9`
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
	-	`sha256:8fd45f8fa7e828bdb5dd8878febd6f367c5092a047db5f6ca094056a1b0c627c`  
		Last Modified: Tue, 14 May 2024 01:24:52 GMT  
		Size: 35.3 MB (35311159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550b27601761a991b3de6e3a4b4e4d50fe6c7ffb31541865520b721cf3746177`  
		Last Modified: Thu, 30 May 2024 03:31:39 GMT  
		Size: 10.3 MB (10276045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c43d86ea69e721acb85f2599759aad0235a69f04a8d7f091a8be4447cba69c4d`  
		Last Modified: Thu, 30 May 2024 03:31:38 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4295834ee6788da085a04107d75cfc88aa66d02f54a1609901cf700be52c48`  
		Last Modified: Thu, 30 May 2024 03:31:43 GMT  
		Size: 32.6 MB (32649905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae11a948e3f0a888ac5e43d357f5a1b0b133be7108e884a68ff43c0b34c0e16`  
		Last Modified: Thu, 30 May 2024 03:31:38 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b73edd05fab5804ef5fa4f8f68f8032bd4f05dfe31f51dad187693b1d1ce324`  
		Last Modified: Thu, 30 May 2024 05:43:36 GMT  
		Size: 28.1 MB (28086522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38b2452960347b3813b6d5f441f05e5f56a7352af83c312237789d581d9c032`  
		Last Modified: Thu, 30 May 2024 05:43:35 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26efb4e0780a37e1b383e1a9a1282701ab9b1ffad52816d5efbde60074a2d601`  
		Last Modified: Thu, 30 May 2024 05:43:35 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dcdd780a4719cce4e8d0fb8fc6951f871efef09fb2a0af8d1e4df3d0ccc77ef`  
		Last Modified: Thu, 30 May 2024 05:43:35 GMT  
		Size: 461.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.2-debian-1.1` - unknown; unknown

```console
$ docker pull fluentd@sha256:12a3829a82e0ad07b4dc862cd64f198ea61710c8edfae92bcea7da28fd0e521c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4110471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d09596edf8142ea948203497f3b17cb65b28f2f246e2d57b98a1755bd7d1d0d`

```dockerfile
```

-	Layers:
	-	`sha256:517e07661428aa4f3149761c9fa80768b88448239b6a3ebb8b7847932535ea01`  
		Last Modified: Thu, 30 May 2024 05:43:35 GMT  
		Size: 4.1 MB (4089337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fd6d73da6f077ad50dc48a66f54224a30c4643b0723c88b3397829a3084c68f`  
		Last Modified: Thu, 30 May 2024 05:43:35 GMT  
		Size: 21.1 KB (21134 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.2-debian-1.1` - linux; s390x

```console
$ docker pull fluentd@sha256:63c1e2d1778cc7d0d84bcbe5dd4413d7e2f8456bf45620473193fbac468449e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98447641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beeebab531289ee35b3a37c37b154440d6c884a5288827feedf2b5b2b6b26aeb`
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
	-	`sha256:14d39445de105c0a8fe00b3899e9fdab7cdfbb3ff27c8b39dd9059f3264a4841`  
		Last Modified: Tue, 14 May 2024 00:48:06 GMT  
		Size: 29.7 MB (29673656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b73b2f4b8a0b336038e774c205e2deaa818f1f9e22bd62b45a8061e0b45008`  
		Last Modified: Thu, 30 May 2024 01:45:07 GMT  
		Size: 8.7 MB (8656975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1a3cca988af307896aeee64218238ef66b6044f4b680960e969a3a7b5572d6`  
		Last Modified: Thu, 30 May 2024 01:45:05 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:660ab6701a0469203cf24e6e0a39e2e6c41af532d2e13e67c00b0dd1d6b8c97c`  
		Last Modified: Thu, 30 May 2024 01:45:06 GMT  
		Size: 32.3 MB (32300418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d1d3a9417752e15732b1aed70f9cdb71862503c260fb1a47ee5434352a53807`  
		Last Modified: Thu, 30 May 2024 01:45:05 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff48d398f8d63ed56755a1f257a4084f9ad307b57112023b4cfd15b46abebd2`  
		Last Modified: Thu, 30 May 2024 03:17:32 GMT  
		Size: 27.8 MB (27813664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d0a537cc9fec20d2ffcb7ea92b9e206a6fa820b8531464863634a95494456d`  
		Last Modified: Thu, 30 May 2024 03:17:31 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1838409b967ce4d3c54b498a212615d5a4cfbab564fcc5c65f10a8ad3ece1705`  
		Last Modified: Thu, 30 May 2024 03:17:31 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0599901586b51a0c7db0f36a1288ff7b59e0d353d9b8cd6f2c30b35d74a9166`  
		Last Modified: Thu, 30 May 2024 03:17:32 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.2-debian-1.1` - unknown; unknown

```console
$ docker pull fluentd@sha256:cf9a594bac147f2d091673e7b22b7b5231f4a83613c0549a2cb92ed1309dc0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4110218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06900592d43cbee03f32ea8ebbac857a5ce24ebb5ad79606396a1b2f7a9ce2b6`

```dockerfile
```

-	Layers:
	-	`sha256:6c34a61d9a7b51d53007fdd392bd3be70b38de01f48158a5b79c01f8b1afa15d`  
		Last Modified: Thu, 30 May 2024 03:17:31 GMT  
		Size: 4.1 MB (4089122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86a620abeb8d1949228f0dd330ed89f2586fe3e116f18a718ebfd33a488dbe98`  
		Last Modified: Thu, 30 May 2024 03:17:31 GMT  
		Size: 21.1 KB (21096 bytes)  
		MIME: application/vnd.in-toto+json
