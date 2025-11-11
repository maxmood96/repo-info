## `openjdk:26-ea-jdk`

```console
$ docker pull openjdk@sha256:7e8e062519b7945a11d290f9ec77b645e80b3e3a5d69ce80bad9dcbf9468632a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.6905; amd64
	-	windows version 10.0.20348.4297; amd64

### `openjdk:26-ea-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:01e6c5849a83abe778fafcdc7489f26c4e76b3a07df27ed47dc3d68c9d8cb698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.4 MB (313427543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1e32f9b52ce76941ac99a5113c29ba966a6b31ff39fc6819896548bfb7b750e`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 17 Oct 2025 22:51:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:51:41 GMT
CMD ["/bin/bash"]
# Mon, 10 Nov 2025 19:53:08 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 10 Nov 2025 19:53:19 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Mon, 10 Nov 2025 19:53:19 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 19:53:19 GMT
ENV LANG=C.UTF-8
# Mon, 10 Nov 2025 19:53:19 GMT
ENV JAVA_VERSION=26-ea+23
# Mon, 10 Nov 2025 19:53:19 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/23/GPL/openjdk-26-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='c5cb587a920ddf65225352cf2494965786acd1de8d6748a976d7498d0783a396'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/23/GPL/openjdk-26-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='427f53a6635347b853f695324253b6d78f69cc09334a9cb1031a801e43358883'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 10 Nov 2025 19:53:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60640e79d279fe0316db1af5ebfd70a728168431645d79005f89dc619ff586f6`  
		Last Modified: Mon, 10 Nov 2025 19:53:57 GMT  
		Size: 38.1 MB (38086182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55c0233a4c209f46c0811ec2c212e0ebd7989ad6be913d650e50c33e60bfaf1`  
		Last Modified: Mon, 10 Nov 2025 22:24:07 GMT  
		Size: 225.8 MB (225844856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:ef67699b28a3871d42d7a3a8d21c09f601eb2995a3cbb1c3c0b3be7c06d458f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3654221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:266facdad2ff0246c17b7056c971da75cae29ff11790510171d45bb91bc20aa4`

```dockerfile
```

-	Layers:
	-	`sha256:419624f5b92bf09352b7204552253c2d61602336e4b63b2045910983d5d638c4`  
		Last Modified: Mon, 10 Nov 2025 22:23:26 GMT  
		Size: 3.6 MB (3636382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a379d3ffc819d5ee8fe5ea374f132541fc933e3175457a6a18f7708528524fa6`  
		Last Modified: Mon, 10 Nov 2025 22:23:27 GMT  
		Size: 17.8 KB (17839 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:9ea1de56d016f68bc6fccafd1d34ba50c615eb82760c275ab524041a26586b09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.3 MB (310278297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ecbf554100a394499239558871dcc1405cf07b1de9c7019ac36b9800df3fde3`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Mon, 10 Nov 2025 19:52:59 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 10 Nov 2025 19:53:09 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Mon, 10 Nov 2025 19:53:09 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 19:53:09 GMT
ENV LANG=C.UTF-8
# Mon, 10 Nov 2025 19:53:09 GMT
ENV JAVA_VERSION=26-ea+23
# Mon, 10 Nov 2025 19:53:09 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/23/GPL/openjdk-26-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='c5cb587a920ddf65225352cf2494965786acd1de8d6748a976d7498d0783a396'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/23/GPL/openjdk-26-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='427f53a6635347b853f695324253b6d78f69cc09334a9cb1031a801e43358883'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 10 Nov 2025 19:53:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01aa7bc1ecdda76fbb99dcf68777bd5b2432a2b3113967e5409b9df0a879716`  
		Last Modified: Mon, 10 Nov 2025 19:53:48 GMT  
		Size: 38.5 MB (38490872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d920c579ae991e390794fbf170533c9a564ab60b59e98a7e2324d131fd70493`  
		Last Modified: Mon, 10 Nov 2025 22:50:20 GMT  
		Size: 223.7 MB (223700524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:a42928ac6c5437e94e237ed2cfc13562824527150a4671c33b6fe9b15ea428ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3652126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28411bbc7c2b21517a858b867e9c3e534dfe8e5b4bb97989bbfc60fcfdd6d12e`

```dockerfile
```

-	Layers:
	-	`sha256:1b16a1581afa6a97d827bb0b24f60984396cf55f6fbc0136e68c62e0465bbaab`  
		Last Modified: Mon, 10 Nov 2025 22:23:31 GMT  
		Size: 3.6 MB (3634072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1d1504a3c738c72dc5020ebc62f50ee33e0d547942f43970d33f746d2f8f0a5`  
		Last Modified: Mon, 10 Nov 2025 22:23:31 GMT  
		Size: 18.1 KB (18054 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk` - windows version 10.0.26100.6905; amd64

```console
$ docker pull openjdk@sha256:9e988a79a99f3252870b9c63baa9924c41eec43d55a1248322c09db69b2dd5d0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 GB (3442864647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:307cd03d71c1e06c03ff9b93640baf308fd60c8c45254b78f5638c42f81b08bd`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Mon, 10 Nov 2025 19:46:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 10 Nov 2025 19:46:53 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 10 Nov 2025 19:46:54 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 10 Nov 2025 19:47:00 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 10 Nov 2025 19:47:01 GMT
ENV JAVA_VERSION=26-ea+23
# Mon, 10 Nov 2025 19:47:02 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/23/GPL/openjdk-26-ea+23_windows-x64_bin.zip
# Mon, 10 Nov 2025 19:47:03 GMT
ENV JAVA_SHA256=41b399a48fae2944ecad52c8f821b2ce5195449fb10eb54a18542b013146fe59
# Mon, 10 Nov 2025 19:47:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 10 Nov 2025 19:47:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bdb4f820c244e1b1c141421c0709d2cf6df07421598eaec46bdb8b9e00226ee`  
		Last Modified: Mon, 10 Nov 2025 19:57:03 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460a64ee5ef62bd9b22d8fb6c5482105f096f1c1d36142358244a7707ffebe90`  
		Last Modified: Mon, 10 Nov 2025 19:57:03 GMT  
		Size: 400.6 KB (400590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8391fe60309ecbb43583542b20f7c9a9b32a431dbef53ce37e9d2805d03ca03`  
		Last Modified: Mon, 10 Nov 2025 19:57:03 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee4182c4a92e8c8ba6c171e45877851a9b63ace11e31cd5aa4f777da768c621`  
		Last Modified: Mon, 10 Nov 2025 19:57:04 GMT  
		Size: 373.8 KB (373849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de0e2857d3eb9d28ab47726fe2732d82146e8e244d110b3b45ee481e09037f7a`  
		Last Modified: Mon, 10 Nov 2025 19:57:04 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739742377babaa48557c238d5a56e9d9595aa38c22f96d6db686c9a74390f7fd`  
		Last Modified: Mon, 10 Nov 2025 19:57:04 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4de729099aa219a7c6ce8e28a538289bc1deaa8307e5553d4c77de6e08f5776`  
		Last Modified: Mon, 10 Nov 2025 19:57:04 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f740d3d4077b5e9c69d8c436fa3b9b288777a3f45331b83ba74e134c501b5fb2`  
		Last Modified: Mon, 10 Nov 2025 22:55:21 GMT  
		Size: 221.7 MB (221735329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4492ec4d1b3c162cfdd22e6b75252131fa34d0cb223d40ccc47d6a9193c41b6a`  
		Last Modified: Mon, 10 Nov 2025 19:57:04 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-ea-jdk` - windows version 10.0.20348.4297; amd64

```console
$ docker pull openjdk@sha256:8d2e7a5d657e291c3d011699f3f4b034ec4b0a5f6e8fbaf42d4bda46483487db
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1799802866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab86cb1f6cc53590fe1e1e5888d70a697b924422e23462b6c9dd748c38745495`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Mon, 10 Nov 2025 19:46:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 10 Nov 2025 19:47:22 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 10 Nov 2025 19:47:22 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 10 Nov 2025 19:47:28 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 10 Nov 2025 19:47:29 GMT
ENV JAVA_VERSION=26-ea+23
# Mon, 10 Nov 2025 19:47:30 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/23/GPL/openjdk-26-ea+23_windows-x64_bin.zip
# Mon, 10 Nov 2025 19:47:30 GMT
ENV JAVA_SHA256=41b399a48fae2944ecad52c8f821b2ce5195449fb10eb54a18542b013146fe59
# Mon, 10 Nov 2025 19:48:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 10 Nov 2025 19:48:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:812bc9a1d91374ca807bd9e023ef98e85f4eddedc06ccf494aa93d48c32cbf4e`  
		Last Modified: Mon, 10 Nov 2025 19:56:04 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:073b2fa8fbf044bb5fe3e9c0fd6d0fc4ddb1520f068d8bd1030f60d905322aff`  
		Last Modified: Mon, 10 Nov 2025 19:56:05 GMT  
		Size: 521.4 KB (521379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a853b7cccb4a6449ea1ae12e5be263e2a9d512ecd63ffccd93daea9c03d0feb`  
		Last Modified: Mon, 10 Nov 2025 19:56:04 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:117b576a54611c7226278fabed13650955d4faa7da407cad54593f79647419bb`  
		Last Modified: Mon, 10 Nov 2025 19:56:05 GMT  
		Size: 360.4 KB (360440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224b16e0e6dab03e17425e3f008ddecbabef7520d422509a6a6269e057a4bc25`  
		Last Modified: Mon, 10 Nov 2025 19:56:04 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a40265931d833b30288e8673aad0353a49660268c26effc33b13d7c981e161`  
		Last Modified: Mon, 10 Nov 2025 19:56:04 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e8b8841b5368eb93445c69cf471741d7ebd33da5e6af735f6595253601c2dab`  
		Last Modified: Mon, 10 Nov 2025 19:56:04 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87a1d24dce9105e2c772bbc8c30902049c482988c811537e462f08c58ab1255`  
		Last Modified: Mon, 10 Nov 2025 22:37:19 GMT  
		Size: 221.7 MB (221720259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a1fa6edffc4342cf9b49f00c3d6495715befceaf4a5651f1ac364a762820ee`  
		Last Modified: Mon, 10 Nov 2025 19:56:06 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
