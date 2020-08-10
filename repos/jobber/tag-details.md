<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `jobber`

-	[`jobber:1.4.4-alpine3.11`](#jobber144-alpine311)
-	[`jobber:1.4-alpine3.11`](#jobber14-alpine311)
-	[`jobber:1-alpine3.11`](#jobber1-alpine311)
-	[`jobber:latest`](#jobberlatest)

## `jobber:1.4.4-alpine3.11`

```console
$ docker pull jobber@sha256:1a45af7aeba09d18680c50c13ea026644d1fc0626b12fd74b63a86c00eacf618
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `jobber:1.4.4-alpine3.11` - linux; amd64

```console
$ docker pull jobber@sha256:f35f7f2fc114f652d0de632fbe7a447b3bea4086cb1433fdad953528e92e1d29
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11760486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6583bbfcfb862dc7a8c53db03383c4b6de0b03c10a9c9270983daaa2ac82ed0`
-	Default Command: `["\/usr\/libexec\/jobberrunner","-u","\/var\/jobber\/1000\/cmd.sock","\/home\/jobberuser\/.jobber"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Wed, 27 May 2020 01:20:08 GMT
ENV USERID=1000
# Wed, 27 May 2020 01:20:09 GMT
RUN addgroup jobberuser &&     adduser -S -u "${USERID}" -G jobberuser jobberuser &&     mkdir -p "/var/jobber/${USERID}" &&     chown -R jobberuser:jobberuser "/var/jobber/${USERID}"
# Mon, 10 Aug 2020 18:23:45 GMT
ENV JOBBER_VERSION=1.4.4
# Mon, 10 Aug 2020 18:23:45 GMT
ENV JOBBER_SHA256=ec09b2efafff69c91fba2124bf28607209e1c9b50ed834ff444a9d40798aa8d3
# Mon, 10 Aug 2020 18:23:47 GMT
RUN wget -O /tmp/jobber.apk "https://github.com/dshearer/jobber/releases/download/v${JOBBER_VERSION}/jobber-${JOBBER_VERSION}-r0.apk" &&     echo -n "Actual checksum: " && sha256sum /tmp/jobber.apk &&     echo "${JOBBER_SHA256} */tmp/jobber.apk" | sha256sum -c &&     apk add --no-network --no-scripts --allow-untrusted /tmp/jobber.apk &&     rm /tmp/jobber.apk
# Mon, 10 Aug 2020 18:23:48 GMT
COPY --chown=jobberuser:jobberuserfile:c7cc6d32091e7beeac78efd9fe855e36a106902c1177df0f9f6bd2bbe3b8d518 in /home/jobberuser/.jobber 
# Mon, 10 Aug 2020 18:23:48 GMT
RUN chmod 0600 /home/jobberuser/.jobber
# Mon, 10 Aug 2020 18:23:49 GMT
USER jobberuser
# Mon, 10 Aug 2020 18:23:49 GMT
CMD ["/usr/libexec/jobberrunner" "-u" "/var/jobber/1000/cmd.sock" "/home/jobberuser/.jobber"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7472975fe6e3c10899344ea80e0a0470a39690e1b83ec11f34e816fa2ae1edef`  
		Last Modified: Wed, 27 May 2020 01:20:19 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa526c9a89b1c967494fcfee44a14465169e6e6ebc5a4417c920b589bb4455f`  
		Last Modified: Mon, 10 Aug 2020 18:23:58 GMT  
		Size: 8.9 MB (8945412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd30cb32f9a2b6c03839149b4316b703b543342b3df8e9d01d4503dfe953ac7`  
		Last Modified: Mon, 10 Aug 2020 18:23:56 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b02c7f528c23007906048b86dec096b08d0f7b77b0f07206e625608a67e673`  
		Last Modified: Mon, 10 Aug 2020 18:23:57 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jobber:1.4-alpine3.11`

```console
$ docker pull jobber@sha256:1a45af7aeba09d18680c50c13ea026644d1fc0626b12fd74b63a86c00eacf618
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `jobber:1.4-alpine3.11` - linux; amd64

```console
$ docker pull jobber@sha256:f35f7f2fc114f652d0de632fbe7a447b3bea4086cb1433fdad953528e92e1d29
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11760486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6583bbfcfb862dc7a8c53db03383c4b6de0b03c10a9c9270983daaa2ac82ed0`
-	Default Command: `["\/usr\/libexec\/jobberrunner","-u","\/var\/jobber\/1000\/cmd.sock","\/home\/jobberuser\/.jobber"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Wed, 27 May 2020 01:20:08 GMT
ENV USERID=1000
# Wed, 27 May 2020 01:20:09 GMT
RUN addgroup jobberuser &&     adduser -S -u "${USERID}" -G jobberuser jobberuser &&     mkdir -p "/var/jobber/${USERID}" &&     chown -R jobberuser:jobberuser "/var/jobber/${USERID}"
# Mon, 10 Aug 2020 18:23:45 GMT
ENV JOBBER_VERSION=1.4.4
# Mon, 10 Aug 2020 18:23:45 GMT
ENV JOBBER_SHA256=ec09b2efafff69c91fba2124bf28607209e1c9b50ed834ff444a9d40798aa8d3
# Mon, 10 Aug 2020 18:23:47 GMT
RUN wget -O /tmp/jobber.apk "https://github.com/dshearer/jobber/releases/download/v${JOBBER_VERSION}/jobber-${JOBBER_VERSION}-r0.apk" &&     echo -n "Actual checksum: " && sha256sum /tmp/jobber.apk &&     echo "${JOBBER_SHA256} */tmp/jobber.apk" | sha256sum -c &&     apk add --no-network --no-scripts --allow-untrusted /tmp/jobber.apk &&     rm /tmp/jobber.apk
# Mon, 10 Aug 2020 18:23:48 GMT
COPY --chown=jobberuser:jobberuserfile:c7cc6d32091e7beeac78efd9fe855e36a106902c1177df0f9f6bd2bbe3b8d518 in /home/jobberuser/.jobber 
# Mon, 10 Aug 2020 18:23:48 GMT
RUN chmod 0600 /home/jobberuser/.jobber
# Mon, 10 Aug 2020 18:23:49 GMT
USER jobberuser
# Mon, 10 Aug 2020 18:23:49 GMT
CMD ["/usr/libexec/jobberrunner" "-u" "/var/jobber/1000/cmd.sock" "/home/jobberuser/.jobber"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7472975fe6e3c10899344ea80e0a0470a39690e1b83ec11f34e816fa2ae1edef`  
		Last Modified: Wed, 27 May 2020 01:20:19 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa526c9a89b1c967494fcfee44a14465169e6e6ebc5a4417c920b589bb4455f`  
		Last Modified: Mon, 10 Aug 2020 18:23:58 GMT  
		Size: 8.9 MB (8945412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd30cb32f9a2b6c03839149b4316b703b543342b3df8e9d01d4503dfe953ac7`  
		Last Modified: Mon, 10 Aug 2020 18:23:56 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b02c7f528c23007906048b86dec096b08d0f7b77b0f07206e625608a67e673`  
		Last Modified: Mon, 10 Aug 2020 18:23:57 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jobber:1-alpine3.11`

```console
$ docker pull jobber@sha256:1a45af7aeba09d18680c50c13ea026644d1fc0626b12fd74b63a86c00eacf618
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `jobber:1-alpine3.11` - linux; amd64

```console
$ docker pull jobber@sha256:f35f7f2fc114f652d0de632fbe7a447b3bea4086cb1433fdad953528e92e1d29
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11760486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6583bbfcfb862dc7a8c53db03383c4b6de0b03c10a9c9270983daaa2ac82ed0`
-	Default Command: `["\/usr\/libexec\/jobberrunner","-u","\/var\/jobber\/1000\/cmd.sock","\/home\/jobberuser\/.jobber"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Wed, 27 May 2020 01:20:08 GMT
ENV USERID=1000
# Wed, 27 May 2020 01:20:09 GMT
RUN addgroup jobberuser &&     adduser -S -u "${USERID}" -G jobberuser jobberuser &&     mkdir -p "/var/jobber/${USERID}" &&     chown -R jobberuser:jobberuser "/var/jobber/${USERID}"
# Mon, 10 Aug 2020 18:23:45 GMT
ENV JOBBER_VERSION=1.4.4
# Mon, 10 Aug 2020 18:23:45 GMT
ENV JOBBER_SHA256=ec09b2efafff69c91fba2124bf28607209e1c9b50ed834ff444a9d40798aa8d3
# Mon, 10 Aug 2020 18:23:47 GMT
RUN wget -O /tmp/jobber.apk "https://github.com/dshearer/jobber/releases/download/v${JOBBER_VERSION}/jobber-${JOBBER_VERSION}-r0.apk" &&     echo -n "Actual checksum: " && sha256sum /tmp/jobber.apk &&     echo "${JOBBER_SHA256} */tmp/jobber.apk" | sha256sum -c &&     apk add --no-network --no-scripts --allow-untrusted /tmp/jobber.apk &&     rm /tmp/jobber.apk
# Mon, 10 Aug 2020 18:23:48 GMT
COPY --chown=jobberuser:jobberuserfile:c7cc6d32091e7beeac78efd9fe855e36a106902c1177df0f9f6bd2bbe3b8d518 in /home/jobberuser/.jobber 
# Mon, 10 Aug 2020 18:23:48 GMT
RUN chmod 0600 /home/jobberuser/.jobber
# Mon, 10 Aug 2020 18:23:49 GMT
USER jobberuser
# Mon, 10 Aug 2020 18:23:49 GMT
CMD ["/usr/libexec/jobberrunner" "-u" "/var/jobber/1000/cmd.sock" "/home/jobberuser/.jobber"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7472975fe6e3c10899344ea80e0a0470a39690e1b83ec11f34e816fa2ae1edef`  
		Last Modified: Wed, 27 May 2020 01:20:19 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa526c9a89b1c967494fcfee44a14465169e6e6ebc5a4417c920b589bb4455f`  
		Last Modified: Mon, 10 Aug 2020 18:23:58 GMT  
		Size: 8.9 MB (8945412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd30cb32f9a2b6c03839149b4316b703b543342b3df8e9d01d4503dfe953ac7`  
		Last Modified: Mon, 10 Aug 2020 18:23:56 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b02c7f528c23007906048b86dec096b08d0f7b77b0f07206e625608a67e673`  
		Last Modified: Mon, 10 Aug 2020 18:23:57 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jobber:latest`

```console
$ docker pull jobber@sha256:1a45af7aeba09d18680c50c13ea026644d1fc0626b12fd74b63a86c00eacf618
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `jobber:latest` - linux; amd64

```console
$ docker pull jobber@sha256:f35f7f2fc114f652d0de632fbe7a447b3bea4086cb1433fdad953528e92e1d29
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11760486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6583bbfcfb862dc7a8c53db03383c4b6de0b03c10a9c9270983daaa2ac82ed0`
-	Default Command: `["\/usr\/libexec\/jobberrunner","-u","\/var\/jobber\/1000\/cmd.sock","\/home\/jobberuser\/.jobber"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Wed, 27 May 2020 01:20:08 GMT
ENV USERID=1000
# Wed, 27 May 2020 01:20:09 GMT
RUN addgroup jobberuser &&     adduser -S -u "${USERID}" -G jobberuser jobberuser &&     mkdir -p "/var/jobber/${USERID}" &&     chown -R jobberuser:jobberuser "/var/jobber/${USERID}"
# Mon, 10 Aug 2020 18:23:45 GMT
ENV JOBBER_VERSION=1.4.4
# Mon, 10 Aug 2020 18:23:45 GMT
ENV JOBBER_SHA256=ec09b2efafff69c91fba2124bf28607209e1c9b50ed834ff444a9d40798aa8d3
# Mon, 10 Aug 2020 18:23:47 GMT
RUN wget -O /tmp/jobber.apk "https://github.com/dshearer/jobber/releases/download/v${JOBBER_VERSION}/jobber-${JOBBER_VERSION}-r0.apk" &&     echo -n "Actual checksum: " && sha256sum /tmp/jobber.apk &&     echo "${JOBBER_SHA256} */tmp/jobber.apk" | sha256sum -c &&     apk add --no-network --no-scripts --allow-untrusted /tmp/jobber.apk &&     rm /tmp/jobber.apk
# Mon, 10 Aug 2020 18:23:48 GMT
COPY --chown=jobberuser:jobberuserfile:c7cc6d32091e7beeac78efd9fe855e36a106902c1177df0f9f6bd2bbe3b8d518 in /home/jobberuser/.jobber 
# Mon, 10 Aug 2020 18:23:48 GMT
RUN chmod 0600 /home/jobberuser/.jobber
# Mon, 10 Aug 2020 18:23:49 GMT
USER jobberuser
# Mon, 10 Aug 2020 18:23:49 GMT
CMD ["/usr/libexec/jobberrunner" "-u" "/var/jobber/1000/cmd.sock" "/home/jobberuser/.jobber"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7472975fe6e3c10899344ea80e0a0470a39690e1b83ec11f34e816fa2ae1edef`  
		Last Modified: Wed, 27 May 2020 01:20:19 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa526c9a89b1c967494fcfee44a14465169e6e6ebc5a4417c920b589bb4455f`  
		Last Modified: Mon, 10 Aug 2020 18:23:58 GMT  
		Size: 8.9 MB (8945412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd30cb32f9a2b6c03839149b4316b703b543342b3df8e9d01d4503dfe953ac7`  
		Last Modified: Mon, 10 Aug 2020 18:23:56 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b02c7f528c23007906048b86dec096b08d0f7b77b0f07206e625608a67e673`  
		Last Modified: Mon, 10 Aug 2020 18:23:57 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
