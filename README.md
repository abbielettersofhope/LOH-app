import React from 'react';
import { NavigationContainer } from '@react-navigation/native';
import { createStackNavigator } from '@react-navigation/stack';
import { View, Text, TouchableOpacity, StyleSheet } from 'react-native';

const Stack = createStackNavigator();

const HomeScreen = ({ navigation }) => {
  return (
    <View style={styles.container}>
      <Text style={styles.header}>Letters of Hope</Text>
      <TouchableOpacity style={styles.button} onPress={() => navigation.navigate('Resources')}>
        <Text style={styles.buttonText}>Mental Health Resources</Text>
      </TouchableOpacity>
      <TouchableOpacity style={styles.button} onPress={() => navigation.navigate('Directory')}>
        <Text style={styles.buttonText}>Service Directory</Text>
      </TouchableOpacity>
      <TouchableOpacity style={styles.button} onPress={() => navigation.navigate('RequestLetter')}>
        <Text style={styles.buttonText}>Request a Letter</Text>
      </TouchableOpacity>
    </View>
  );
};

const ResourcesScreen = () => (
  <View style={styles.container}><Text style={styles.header}>Mental Health Resources</Text></View>
);

const DirectoryScreen = () => (
  <View style={styles.container}><Text style={styles.header}>Service Directory</Text></View>
);

const RequestLetterScreen = () => (
  <View style={styles.container}><Text style={styles.header}>Request a Letter</Text></View>
);

export default function App() {
  return (
    <NavigationContainer>
      <Stack.Navigator initialRouteName="Home">
        <Stack.Screen name="Home" component={HomeScreen} options={{ headerShown: false }} />
        <Stack.Screen name="Resources" component={ResourcesScreen} />
        <Stack.Screen name="Directory" component={DirectoryScreen} />
        <Stack.Screen name="RequestLetter" component={RequestLetterScreen} />
      </Stack.Navigator>
    </NavigationContainer>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    justifyContent: 'center',
    alignItems: 'center',
    backgroundColor: '#F1F8F6',
  },
  header: {
    fontSize: 24,
    fontWeight: 'bold',
    color: '#545454',
    marginBottom: 20,
  },
  button: {
    backgroundColor: '#9FC8BC',
    padding: 15,
    margin: 10,
    borderRadius: 10,
    width: '80%',
    alignItems: 'center',
  },
  buttonText: {
    color: '#FFFFFF',
    fontSize: 16,
    fontWeight: 'bold',
  },
});


