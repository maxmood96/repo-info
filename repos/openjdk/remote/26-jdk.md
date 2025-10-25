## `openjdk:26-jdk`

```console
$ docker pull openjdk@sha256:0640fcc10dfe7542ab6b94de8979fefdc5aece0f4360abaa28bbab117f169d4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.6905; amd64
	-	windows version 10.0.20348.4297; amd64

### `openjdk:26-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:8d7c378765a71534f01b7282f8a5e3b34cd0c9214762151f77468ba417026c2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.3 MB (313253484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:623e9b73c742e68499824e9d0a93e2de15804b3cf7a2cf31a97c4d44aedc9142`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 17 Oct 2025 22:51:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:51:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Oct 2025 18:48:18 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 20 Oct 2025 18:48:18 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Mon, 20 Oct 2025 18:48:18 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Oct 2025 18:48:18 GMT
ENV LANG=C.UTF-8
# Mon, 20 Oct 2025 18:48:18 GMT
ENV JAVA_VERSION=26-ea+20
# Mon, 20 Oct 2025 18:48:18 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/20/GPL/openjdk-26-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='5a59bcbbbee3ef3870abde737d101b8688ff06144c853ff29ef6ac8247c96a87'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/20/GPL/openjdk-26-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='bf2a13c36da561391ccbda5d5d8dcce3963d35f2d5b0819a1fa725999f090aa4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 20 Oct 2025 18:48:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c866b10aa84572d6ccbe9ede1c14e6efb6e2dbe1cdecfdd5070cae2ea27f72`  
		Last Modified: Tue, 21 Oct 2025 20:20:42 GMT  
		Size: 38.1 MB (38087689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0597ba46067f9c883e71e3c80c84ae2224b43600a53b6f1771d77742a04008b`  
		Last Modified: Tue, 21 Oct 2025 21:30:18 GMT  
		Size: 225.7 MB (225669290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:4a5ed51e5f0b75cfa7223f23a55bb679803f9d9cdcd772af5ed0339b28769677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3659243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee96783f628f0a03477b012f9829f231a80c0f460edb5900307d4615e6fe1053`

```dockerfile
```

-	Layers:
	-	`sha256:2e85abe5da17d804ae255cbb6412ec25ba6e2292cd27124782bc016ec37888ed`  
		Last Modified: Tue, 21 Oct 2025 21:23:26 GMT  
		Size: 3.6 MB (3639498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e739561f92386c76f77e10b96b5b5c43ebccd49b14b31f997c504abe4546dd4`  
		Last Modified: Tue, 21 Oct 2025 21:23:26 GMT  
		Size: 19.7 KB (19745 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:80f0e92ed6f4d4d80f4ffd9170ac79a4a35d56298cac5304e9c64db3ac672a1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.1 MB (310109383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ca318e0c6b372994880cbacf95242d4533226be5a44dc6070af01c09ef2bbe7`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Mon, 20 Oct 2025 18:48:18 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 20 Oct 2025 18:48:18 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Mon, 20 Oct 2025 18:48:18 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Oct 2025 18:48:18 GMT
ENV LANG=C.UTF-8
# Mon, 20 Oct 2025 18:48:18 GMT
ENV JAVA_VERSION=26-ea+20
# Mon, 20 Oct 2025 18:48:18 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/20/GPL/openjdk-26-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='5a59bcbbbee3ef3870abde737d101b8688ff06144c853ff29ef6ac8247c96a87'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/20/GPL/openjdk-26-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='bf2a13c36da561391ccbda5d5d8dcce3963d35f2d5b0819a1fa725999f090aa4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 20 Oct 2025 18:48:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7abf9b5ac6e04ae79429ac398f1c36fe0800241f536cfec4212e43951406c4f`  
		Last Modified: Tue, 21 Oct 2025 18:13:51 GMT  
		Size: 38.5 MB (38491195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e27c39ec2fc86bde4248d7676af7a1be3e098446bed593adc792141beaec2ce`  
		Last Modified: Tue, 21 Oct 2025 21:37:02 GMT  
		Size: 223.5 MB (223531287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:b06072fd086447aff33d4b1f6c8a71d7dbd056a704f61ebbb0ffe264c55b1560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3657293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb747b7cf2206f08db68e772b32efccc04a2dee17c68bcd22141c2e131e2e4e6`

```dockerfile
```

-	Layers:
	-	`sha256:4671df4d1762f10bb5f78ef01f1eb575481a26ade2f2725da736e05be92eea9d`  
		Last Modified: Tue, 21 Oct 2025 21:23:31 GMT  
		Size: 3.6 MB (3637260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbb4c00d5b889a7d6b210c9cfcf3e20358d77a6b441af78d33880dadf7bf1150`  
		Last Modified: Tue, 21 Oct 2025 21:23:31 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-jdk` - windows version 10.0.26100.6905; amd64

```console
$ docker pull openjdk@sha256:dcaf1b0fcb10da8796f5e3995ce88ddce631d60fcf93c9fd0b74db5c0db89ea4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 GB (3442588550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df30acd51fb7d80fdd310d0958b10fe94753801c489fc7a6673fb1083e55fb64`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Fri, 24 Oct 2025 18:13:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:25:51 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:25:52 GMT
ENV JAVA_HOME=C:\openjdk-26
# Fri, 24 Oct 2025 18:25:57 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:25:58 GMT
ENV JAVA_VERSION=26-ea+20
# Fri, 24 Oct 2025 18:25:58 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/20/GPL/openjdk-26-ea+20_windows-x64_bin.zip
# Fri, 24 Oct 2025 18:25:59 GMT
ENV JAVA_SHA256=dbd547c391f90daa966d5d3a236e5a3cf792dea341d9596eb2a155059fe571a1
# Fri, 24 Oct 2025 18:26:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:26:20 GMT
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
	-	`sha256:571af3b90b3defe521c8285732a5f27a7d3abdaa40750b1b3e6b3d6208a2b69d`  
		Last Modified: Fri, 24 Oct 2025 18:23:19 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63342a0df8c3b04da2641155654f3abb2efd56e5631d876efd52b593ded2533e`  
		Last Modified: Fri, 24 Oct 2025 18:26:47 GMT  
		Size: 357.3 KB (357257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:778674c5686153fd6b36a9dce761dd8d20054eae0ac61ec44dc9990e84afa732`  
		Last Modified: Fri, 24 Oct 2025 18:26:47 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509fa57fff4e53c6a15dc770524ac1915eb558c250371f1fab8177c48c85bee2`  
		Last Modified: Fri, 24 Oct 2025 18:26:47 GMT  
		Size: 339.9 KB (339859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415656e85a86621f67a54d2f4580c516da12bed96b4b70919b275baa66d3e033`  
		Last Modified: Fri, 24 Oct 2025 18:26:47 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b0b4804f525525dbfc6675fabde05c6aa78a4e69fe543eff6d529d1eb3e979`  
		Last Modified: Fri, 24 Oct 2025 18:26:47 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f4143e4d79f6d99ae2b1bfa65167a789d64367ecd72eb819142ccca08a0b18`  
		Last Modified: Fri, 24 Oct 2025 18:26:47 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e15882bb296b95dc8e2c193f8548e10e565b2b1331985ae12f75b576e0f3c9`  
		Last Modified: Fri, 24 Oct 2025 19:22:23 GMT  
		Size: 221.5 MB (221536571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a5769a93539dbd680ec29a6ec9b65125efda73eb2831a4dc1fe17de224a154`  
		Last Modified: Fri, 24 Oct 2025 18:26:47 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-jdk` - windows version 10.0.20348.4297; amd64

```console
$ docker pull openjdk@sha256:920f5c63d0c9a0eef0e53b82f3bfb03f642d452d86fd57fd4bd116e9d22e6e60
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1799572711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce48e935e5c72441eee6e2f45f834efe6b357797b79c81b02a273d47f9e339c0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:10:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:25:18 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:25:19 GMT
ENV JAVA_HOME=C:\openjdk-26
# Fri, 24 Oct 2025 18:25:24 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:25:25 GMT
ENV JAVA_VERSION=26-ea+20
# Fri, 24 Oct 2025 18:25:26 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/20/GPL/openjdk-26-ea+20_windows-x64_bin.zip
# Fri, 24 Oct 2025 18:25:27 GMT
ENV JAVA_SHA256=dbd547c391f90daa966d5d3a236e5a3cf792dea341d9596eb2a155059fe571a1
# Fri, 24 Oct 2025 18:25:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:26:01 GMT
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
	-	`sha256:116a61045287ead6d3e96e549433b65e0cd74ce2180f5ec4df258d66b09b85a4`  
		Last Modified: Fri, 24 Oct 2025 18:20:52 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1965ee7d4e5941254fb504bbf07a4d846c8116a09543cba0b5dd6a02dd409afd`  
		Last Modified: Fri, 24 Oct 2025 18:26:27 GMT  
		Size: 493.1 KB (493131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b85c552306b194d12184edfc57f11620f4383e3e211e30f804ecc2c62b3daf45`  
		Last Modified: Fri, 24 Oct 2025 18:26:27 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b2b5536b51c7e63ab0aaa7b83c1ce821c45bacbe94eecfa84d1bc905ee4fbe`  
		Last Modified: Fri, 24 Oct 2025 18:26:27 GMT  
		Size: 335.0 KB (335007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c6b48d4b9e27041f607e7788cacf2a1014a2b43034c941e117e70267d2e3e1`  
		Last Modified: Fri, 24 Oct 2025 18:26:27 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a51cee5eca8ba1661d9a9d0aaf49f7e160a3f57b3c082a26e49764644d977f09`  
		Last Modified: Fri, 24 Oct 2025 18:26:27 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281720dc0cebc19f7f111c9214ae5141953a3670e2135c7858d72a05b821fde5`  
		Last Modified: Fri, 24 Oct 2025 18:26:27 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed9e5b921041249c96fa258465845aa39e5326cc1ed747dbdeb5e71241beede6`  
		Last Modified: Fri, 24 Oct 2025 19:20:31 GMT  
		Size: 221.5 MB (221543812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2217eb78e443602f482082162a9636ac0f1e367296905bd9e618a23ad0fc0af`  
		Last Modified: Fri, 24 Oct 2025 18:26:27 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
