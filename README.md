import React from 'react';

const App = () => {
  return (
    <div style={styles.container}>
      <h1 style={styles.header}>Letters of Hope</h1>
      <button style={styles.button} onClick={() => alert('Navigating to Mental Health Resources')}>
        Mental Health Resources
      </button>
      <button style={styles.button} onClick={() => alert('Navigating to Service Directory')}>
        Service Directory
      </button>
      <button style={styles.button} onClick={() => alert('Navigating to Request a Letter')}>
        Request a Letter
      </button>
    </div>
  );
};

const styles = {
  container: {
    display: 'flex',
    flexDirection: 'column',
    alignItems: 'center',
    justifyContent: 'center',
    height: '100vh',
    backgroundColor: '#F1F8F6',
    fontFamily: 'Arial, sans-serif',
  },
  header: {
    fontSize: '24px',
    fontWeight: 'bold',
    color: '#545454',
    marginBottom: '20px',
  },
  button: {
    backgroundColor: '#9FC8BC',
    color: '#FFFFFF',
    fontSize: '16px',
    fontWeight: 'bold',
    padding: '15px',
    margin: '10px',
    border: 'none',
    borderRadius: '10px',
    cursor: 'pointer',
    width: '80%',
    maxWidth: '300px',
  },
};

export default App;
