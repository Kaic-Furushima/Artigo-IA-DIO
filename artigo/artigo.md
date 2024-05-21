<p align="center">
    <img src="./Remodelando o Mundo Quadrado.png" alt="Banner principal">
</p>

Então você está interessado em criar seus próprios mods para minecraft? Incrível! Mods são pequenas modificações no jogo que você pode fazer para adicionar novas coisas ou mudar como o jogo funciona. Vamos aprender o básico de como fazer isso de uma forma bem simples.

O que Você Vai Precisar:
- Minecraft Java Edition: Mods são feitos para essa versão do jogo.
- Java Development Kit (JDK): É um programa que ajuda a escrever e testar código em Java, a linguagem usada para criar mods.
- Forge: Uma ferramenta que facilita a criação de mods.
- Um editor de texto: Pode ser algo simples como o Bloco de Notas ou algo mais avançado como o VS Code.

##
<p align="center">
    <img src="./Remodelando o Mundo Quadrado (1).png" alt="Banner secundário 1">
</p>

## Instalar o JDK

Primeiro, você precisa instalar o JDK. Procure por "JDK download" no Google, baixe e instale no seu computador. Isso é importante para poder escrever e executar código em Java.

## Instalar o Forge

O Forge é uma ferramenta que ajuda a criar e rodar mods. Visite o site oficial do Forge e baixe a versão que corresponde à versão do seu Minecraft.

## Crie uma pasta para o seu projeto 
- Dê um nome legal, tipo "MeusPrimeirosMods".
- Abra a pasta no editor de texto. Se estiver usando o VS Code, clique em "Abrir Pasta" e selecione sua pasta.
- Baixe o MDK (Mod Development Kit) do Forge e descompacte o conteúdo dentro da pasta do seu projeto.

##
<p align="center">
    <img src="./Remodelando o Mundo Quadrado (2).png" alt="Banner secundário 2">
</p>

## Criar Seu Primeiro Mod
Dentro da pasta do seu projeto, você verá muitos arquivos e pastas. Não se assuste! Vamos focar nos principais:

- src/main/java: Aqui é onde você vai escrever o código do seu mod.
- src/main/resources: Aqui você coloca os recursos como texturas e arquivos de configuração.
## Escrever o Código
Vamos criar um mod simples que adiciona um novo item no jogo. No editor de texto, navegue até a pasta src/main/java e crie um pacote (pasta) chamado com.seumod. Dentro dessa pasta, crie um arquivo chamado Main.java.

Aqui está um exemplo de código simples para adicionar um item:

```java

package com.seumod;

import net.minecraft.item.Item;
import net.minecraft.item.ItemGroup;
import net.minecraftforge.api.distmarker.Dist;
import net.minecraftforge.event.RegistryEvent;
import net.minecraftforge.eventbus.api.SubscribeEvent;
import net.minecraftforge.fml.common.Mod;
import net.minecraftforge.fml.event.lifecycle.FMLClientSetupEvent;
import net.minecraftforge.fml.event.lifecycle.FMLCommonSetupEvent;
import net.minecraftforge.fml.common.Mod.EventBusSubscriber;
import net.minecraftforge.registries.ObjectHolder;

@Mod("seumod")
public class Main {
    public Main() {
        // Registro de eventos
    }

    @EventBusSubscriber(bus = EventBusSubscriber.Bus.MOD)
    public static class RegistryEvents {
        @SubscribeEvent
        public static void registerItems(final RegistryEvent.Register<Item> event) {
            event.getRegistry().registerAll(
                new Item(new Item.Properties().group(ItemGroup.MISC)).setRegistryName("seumod", "item_legal")
            );
        }
    }
}

```
##
<p align="center">
    <img src="./Remodelando o Mundo Quadrado (3).png" alt="Banner secundário 3">
</p>

## Personalizar Seu Mod

Agora que você sabe o básico, pode explorar mais! Adicione mais itens, crie blocos novos, ou até mesmo animais! Existem muitos tutoriais online que podem ajudar a expandir seu conhecimento.

## Dicas Finais
- Aprenda Java: Quanto mais você souber sobre a linguagem de programação Java, mais coisas legais poderá fazer.
- Procure Tutoriais: O YouTube e fóruns de Minecraft têm muitos tutoriais para ajudar.
- Divirta-se: Criar mods deve ser divertido, então experimente e veja o que você consegue criar!

Boa sorte e divirta-se criando seus mods para Minecraft!
