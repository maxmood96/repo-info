## `golang:nanoserver-1809`

```console
$ docker pull golang@sha256:93aaff60c6b414b2e928eaacd6513d781ec58fd31859b025b33064a8f2b32711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `golang:nanoserver-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull golang@sha256:509e5654c998b63fe2d798f3ca472b8d88b7c763ab8d5bfe9354fc220a3433b1
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173827549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dc88fb22576609acf0da588656fccabe15ae1f7fd8e21ad610b07c12a2f1525`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Wed, 10 Jan 2024 23:35:47 GMT
SHELL [cmd /S /C]
# Wed, 10 Jan 2024 23:35:48 GMT
ENV GOPATH=C:\go
# Wed, 10 Jan 2024 23:35:48 GMT
USER ContainerAdministrator
# Wed, 10 Jan 2024 23:35:58 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 10 Jan 2024 23:35:59 GMT
USER ContainerUser
# Tue, 06 Feb 2024 20:24:14 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 20:25:59 GMT
COPY dir:5ff7da3e893fb14a7305ba69003260f08dbd1259ee061bba7a41a59602fd7180 in C:\Program Files\Go 
# Tue, 06 Feb 2024 20:26:25 GMT
RUN go version
# Tue, 06 Feb 2024 20:26:26 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f4359fc279f6237926816561ae1d2b91635d62f4054c41225432d1e891648a1`  
		Last Modified: Thu, 11 Jan 2024 00:05:11 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b82c9961fa54075d432c10bfadc90379a518456fb02e499df24a877541ac94`  
		Last Modified: Thu, 11 Jan 2024 00:05:11 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28323fdaacc7793676850ff73c132c20076785bf195fa0399ca7f38d71126f5`  
		Last Modified: Thu, 11 Jan 2024 00:05:11 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0130ba848c13896810ce8496ef1b534ba38a9f82a6b7e8585c8c2060721ad52f`  
		Last Modified: Thu, 11 Jan 2024 00:05:10 GMT  
		Size: 68.6 KB (68647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b417f6b6e79c03bf6187db98994d1da138adad475d8e228b80bcf55b4a08622`  
		Last Modified: Thu, 11 Jan 2024 00:05:08 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26037a90b7de1910455bdb26ae21e607ec722f478820bd0730b337c98509e8ee`  
		Last Modified: Tue, 06 Feb 2024 20:40:02 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b69804009e9d492706b3bd78d968ac93d3fa3bcb1907143cd8ad1dd9f4575c7`  
		Last Modified: Tue, 06 Feb 2024 20:40:20 GMT  
		Size: 69.1 MB (69088761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10bdb5598e9641d6dea3bfda2a4d069a3e27ea3af45edc5016aa30c0aa7b49ca`  
		Last Modified: Tue, 06 Feb 2024 20:40:03 GMT  
		Size: 71.8 KB (71772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec9a303302c0a1fd3e16084a5da0d1cdfa6d8439f0d7b02bf55b0e0784a63ace`  
		Last Modified: Tue, 06 Feb 2024 20:40:02 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
